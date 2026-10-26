# Project: LoL Item Advisor

## Users

The primary users are casual and beginner League of Legends players who want help choosing suitable items against specific enemy team compositions.

The application is also intended for:

- **Bronze to Platinum players:** Players who want to improve their itemization and in-game decision-making.
- **Players unfamiliar with all item effects:** Players who need help understanding which items are effective in different situations.
- **Players using a phone while playing on a PC:** Players who want quick access to item recommendations without searching through multiple websites.

## MVP

The application will allow users to select their champion, choose between one and five enemy champions, and receive item recommendations based on the enemy team's composition.

The MVP will include:

- Champion selection with a search function and champion icons.
- Selection of one to five enemy champions.
- A summary of the enemy team's characteristics, including physical damage, magic damage, crowd control, healing, and tankiness.
- Item recommendations based on predefined rules.
- Item names, icons, prices, and basic descriptions.
- Short explanations of why each item is recommended.
- A responsive user interface designed primarily for mobile devices.
- Access to champion and item information using Riot Data Dragon.

The recommendations will be based on custom rules stored in local JSON files. Champion and item information will be retrieved from Riot Data Dragon.

The application will run as a web application and will not require users to create an account.

As an extension of the MVP, the application may support saving builds locally, suggesting counterpicks, and installation as a Progressive Web App (PWA).

## Non-goals

The initial version of the application will not include:

- **Live match analysis:** The application will not automatically detect the current match or analyze live game data.
- **Screenshot recognition:** Champion recognition from screenshots will not be implemented in the initial version.
- **AI-generated recommendations:** Recommendations will be based on predefined rules rather than generative AI.
- **Win rate statistics:** The application will not provide champion or item recommendations based on live win rate statistics.
- **User accounts:** Registration and user authentication will not be required.
- **Cloud synchronization:** User data and saved builds will not be synchronized between devices.
- **Social features:** The application will not include profiles, comments, or community features.
- **Push notifications:** Patch notifications and other notifications will be outside the scope of the MVP.
- **Native iOS and Android applications:** The initial version will be developed as a web application accessible through a browser.

These features are excluded to keep the initial implementation focused on helping players make better itemization decisions quickly and easily.

## Technologies

### Frontend

- **HTML:** Used to structure the web application.
- **CSS:** Used to style the interface and create a responsive layout.
- **JavaScript or TypeScript:** Used to implement the application logic, process champion data, and generate item recommendations.
- **React:** Used to build reusable interface components and manage application state.

### Data Sources

- **Riot Data Dragon:** Used to retrieve champion and item information, including names, icons, descriptions, and item prices.
- **JSON:** Used to store custom champion characteristics, item properties, counter relationships, and recommendation rules.

### Local Storage

- **Browser Local Storage:** Used to store simple user preferences and, in a later version, saved builds locally.
- **JSON files:** Used to provide predefined recommendation rules without requiring a backend database.

### Additional Tools

- **Visual Studio Code:** Used as the development environment.
- **Git:** Used for version control.
- **GitHub:** Used to host the source code.
- **Vercel or GitHub Pages:** Potential options for deploying the web application.

### Architecture

The initial version will use a frontend-only architecture without a custom backend.

Champion and item information will be retrieved from Riot Data Dragon, while the recommendation engine will process locally stored JSON rules.

The application will analyze the selected enemy team and generate recommendations directly in the browser.

User accounts and server-side data storage will not be required for the MVP.

The interface will follow a mobile-first approach so that players can use the application comfortably on their phones while playing League of Legends on a computer.

## Initiative

**Help League of Legends players make better itemization decisions by providing fast, understandable, and situation-specific recommendations.**

The main objective is to simplify item selection and help players understand how to adapt their builds to different enemy team compositions.

The application should provide useful recommendations in less than 30 seconds after the user selects their champion and the enemy team.

## Epics

### Epic 1: Champion Selection

Allow users to select their own champion and the enemy champions they are playing against.

#### User Story 1

As a player, I want to search for and select my champion so that I can receive recommendations relevant to my character.

**Tasks:**
- Retrieve champion data from Riot Data Dragon.
- Create a searchable champion selection interface.
- Display champion names and icons.
- Store the selected champion in the application state.
- Allow users to change their selection.

#### User Story 2

As a player, I want to select between one and five enemy champions so that the application can analyze the opposing team.

**Tasks:**
- Implement multiple champion selection.
- Display the selected enemy champions.
- Prevent duplicate selections.
- Allow users to remove selected champions.
- Provide a reset option for the enemy team selection.

### Epic 2: Enemy Team Analysis

Analyze the selected enemy team to identify its most important characteristics.

#### User Story 3

As a player, I want to see whether the enemy team relies more on physical or magic damage so that I can choose appropriate defensive items.

**Tasks:**
- Create a JSON dataset containing champion damage characteristics.
- Implement enemy team composition analysis.
- Calculate a simplified physical and magic damage profile.
- Display the results using a visual indicator or progress bar.

#### User Story 4

As a player, I want to identify threats such as crowd control, healing, and tankiness so that I can adapt my build to the enemy team.

**Tasks:**
- Define champion characteristics such as crowd control, healing, burst damage, and tankiness.
- Implement rules for identifying important team composition threats.
- Define thresholds for highlighting specific threats.
- Display warning labels for relevant enemy team characteristics.

### Epic 3: Item Recommendations

Recommend items that address the main threats identified in the enemy team composition.

#### User Story 5

As a player, I want to receive item recommendations based on the enemy team so that I can make better purchasing decisions.

**Tasks:**
- Create a JSON dataset containing item properties and recommendation rules.
- Implement the recommendation engine.
- Match enemy team characteristics to relevant items.
- Display recommended items with their icons, names, and prices.
- Prioritize recommendations based on their relevance to the selected situation.

#### User Story 6

As a player, I want to understand why an item is recommended so that I can learn how to make better itemization decisions.

**Tasks:**
- Create short explanations for each recommendation rule.
- Display the explanation on each recommended item card.
- Highlight the enemy team characteristics that triggered the recommendation.
- Ensure that recommendations are understandable to beginner players.

#### User Story 7

As a player, I want to see which items are suitable for different stages of my build so that I can plan my purchases more effectively.

**Tasks:**
- Define categories for starting, core, and situational items.
- Implement a basic build recommendation structure.
- Display recommended items in separate categories.
- Explain when a situational item may be useful.

### Epic 4: Counterpick Recommendations

Help users identify champions that may perform well against a selected enemy champion.

This epic is planned as a future extension and is not required for the initial MVP.

#### User Story 8

As a player, I want to see potential counterpicks against an enemy champion so that I can make a more informed champion selection.

**Tasks:**
- Create a JSON dataset containing predefined counter relationships.
- Implement a champion detail view.
- Display three to five potential counterpicks.
- Provide short explanations for each counterpick.

### Epic 5: Saved Builds

Allow users to save and reuse useful item builds.

This epic is planned as a future extension.

#### User Story 9

As a player, I want to save my preferred builds so that I can access them again without repeating the selection process.

**Tasks:**
- Define a data model for saved builds.
- Store builds in browser Local Storage.
- Display a list of saved builds.
- Allow users to rename and delete saved builds.
- Restore a saved build when selected.

#### User Story 10

As a player, I want to share a build through a link so that another player can view the same recommendations.

**Tasks:**
- Encode the selected champion and build information into URL parameters.
- Generate a shareable URL.
- Load the selected build when the URL is opened.
- Validate URL parameters before displaying the build.

### Epic 6: Mobile Experience and PWA

Make the application convenient to use on a mobile phone while playing League of Legends on a computer.

#### User Story 11

As a player, I want to use the application comfortably on my phone so that I can quickly check item recommendations during a match.

**Tasks:**
- Implement a responsive, mobile-first interface.
- Optimize champion selection for touch interaction.
- Display item recommendations in a compact layout.
- Minimize the number of steps required to obtain recommendations.
- Test the application on different screen sizes.

#### User Story 12

As a player, I want to install the application on my phone so that I can access it like a regular application without downloading it from an app store.

**Tasks:**
- Create a web app manifest.
- Configure the application for Progressive Web App installation.
- Implement a service worker for caching suitable application resources.
- Provide basic offline access to previously cached data where possible.
- Test installation and application behavior on supported mobile browsers.

## MVP Success Criteria

The MVP will be considered successful if users can:

- Select their own champion.
- Select one to five enemy champions.
- View a summary of the enemy team's characteristics.
- Receive relevant item recommendations.
- Understand why each recommended item is useful.
- Complete the main workflow in less than 30 seconds.
- Use the application on both desktop and mobile browsers without creating an account.

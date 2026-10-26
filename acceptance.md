# ACCEPTANCE.md

## 1. Champion Selection

### AC-1.1 Search for Own Champion
- The user can search for a champion by name.
- Matching results are displayed when the user enters a champion name.
- After a champion is selected, its name and icon are displayed in the own champion section.
- If no champion matches the search query, the application displays a message indicating that no results were found.

### AC-1.2 Select Enemy Champions
- The user can select a minimum of one and a maximum of five enemy champions.
- Each selected enemy champion is displayed with its name and icon.
- The same enemy champion cannot be added more than once.
- After five enemy champions have been selected, the application prevents the user from adding another.
- The user can remove an individual enemy champion from the selection.
- The user can remove all selected enemy champions at once.

## 2. Enemy Team Analysis

### AC-2.1 Physical and Magic Damage
- After enemy champions are selected, the application displays the estimated distribution of physical and magic damage.
- The physical and magic damage percentages add up to 100% when all required data is available.
- If required analysis data is missing, the application informs the user and does not automatically treat missing values as zero damage.

### AC-2.2 Enemy Threats
- The application displays indicators for relevant threats, such as crowd control (CC), healing, and durability or tankiness.
- Each indicator is based on defined data about the selected enemy champions.
- If there is insufficient data to assess a threat, the application marks the result as unknown instead of indicating that the threat does not exist.

## 3. Item Recommendations

### AC-3.1 Generate Recommendations
- After the user selects their own champion and at least one enemy champion, the application displays recommended items if matching rules exist.
- Recommendations take both the user's champion and the enemy team composition into account.
- Each recommended item includes its name, icon, price, and an explanation of why it is recommended.
- Each recommended item belongs to one of the following categories: starter, core, or situational.
- If no suitable items are found, the application displays a clear message instead of an empty or broken screen.
- The application does not display an item whose identifier is invalid or missing from the loaded item data.

### AC-3.2 Update Recommendations
- When the user changes their own champion or the selected enemies, the application updates the analysis and item recommendations.
- Recommendations reflect the current champion selection and do not display results from a previous selection.

## 4. Counterpick Recommendations

### AC-4.1 Recommend Champions
- The application displays up to five recommended counterpick champions based on the selected enemies and available rules.
- Each recommended champion includes its name and an explanation of why it may be effective against the selected enemy team.
- The application only displays champions that exist in the loaded champion data.
- If no suitable counterpicks are available, the application displays a message indicating that no recommendations are available.

## 5. Build Saving and Sharing

### AC-5.1 Save Builds
- The user can save the current champion selection and related build information under a chosen name.
- After saving, the build appears in the saved builds list.
- A saved build remains available after the page is refreshed in the same browser profile, unless it is deleted or the browser data is cleared.
- The user can rename a saved build.
- The user can delete a saved build.
- After deletion, the build no longer appears in the saved builds list.

### AC-5.2 Share Builds
- The user can generate a URL containing the information required to restore a shared champion selection.
- When a valid shared URL is opened, the application restores the own champion and the selected enemy champions.
- After restoring the selection, the application calculates recommendations using the currently available rules and data.
- If a URL contains invalid or unknown identifiers, the application safely rejects them and displays a clear message.
- A shared build can be opened in another browser without access to the original user's locally saved builds.

## 6. Mobile and Desktop Layout

### AC-6.1 Responsive Interface
- The application is usable on both mobile devices and desktop computers.
- At a viewport width of 320 CSS pixels, the user can access champion selection, analysis, and recommendations without horizontal scrolling of the entire page.
- Text, icons, and controls remain readable and do not overlap.
- All main features can be operated using both a touchscreen and a mouse.

## 7. Offline Mode and Data Loading

### AC-7.1 Load Data
- When Riot Data Dragon is available, the application loads the required champion and item data.
- If the data cannot be loaded, the application displays a clear error message.
- A failure to load external data does not cause an unhandled application crash.

### AC-7.2 Offline Usage
- After the application has been loaded successfully, its cached application shell remains accessible offline if a service worker has been implemented and is functioning correctly.
- If the required data is available in the cache, the application can use it without an internet connection.
- If required data is not cached, the application informs the user that the relevant feature is currently unavailable.

## 8. General Requirements

- The application can be used without creating an account or signing in.
- Saved builds are stored locally in the browser and are not sent to a custom backend.
- Invalid inputs and missing data do not cause an unhandled application failure.
- Text obtained from external data is rendered safely and is not executed as HTML or JavaScript.
- The main features can be tested without a database or custom backend.



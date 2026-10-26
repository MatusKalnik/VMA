# SPEC.md — LoL Item Advisor

## Problem

League of Legends players often struggle to choose suitable items and counterpicks against specific enemy team compositions. This can lead to ineffective itemization decisions during champion selection and matches.

LoL Item Advisor aims to help players make faster and more informed decisions by providing item recommendations, explaining their benefits, and highlighting important characteristics of the enemy team.

## Users and Roles

- **Player:** The only user role. Players can select champions, analyze enemy team compositions, view item recommendations, explore counterpicks, and save builds without creating an account.
- **Developer:** Maintains champion characteristics, item properties, recommendation rules, and counterpick data outside the application. There is no administrator role within the application.

The target audience includes casual and beginner players, Bronze to Platinum players, and players who use a mobile device alongside their PC while playing League of Legends.

## Features

### 1. Champion Selection

- **1.1** Players can search for and select their own champion.
- **1.2** Players can select between one and five enemy champions.
- **1.3** Players can remove individual enemy champions or reset the entire selection.

### 2. Enemy Team Analysis

- **2.1** Players can view an overview of the enemy team's physical (AD) and magic (AP) damage characteristics.
- **2.2** Players can see indicators for important enemy team threats, including crowd control, healing, and tankiness.

### 3. Item Recommendations

- **3.1** Players receive item recommendations based on their selected champion and the enemy team composition.
- **3.2** Players can see a short explanation of why each item is recommended.
- **3.3** Players can view recommended items grouped into starting, core, and situational categories.
- **3.4** Players can view each recommended item's name, icon, price, and basic information.

### 4. Counterpick Recommendations

- **4.1** Players can view three to five potential counterpicks against a selected enemy champion.
- **4.2** Players can read a short explanation of why each counterpick may be effective.

### 5. Build Management and Sharing

- **5.1** Players can save a build containing their selected champion and enemy team composition.
- **5.2** Players can view, rename, and delete their saved builds.
- **5.3** Players can share a build through a URL that allows another player to open the same selection and view its recommendations.

### 6. Cross-Device Usage

- **6.1** Players can use the application on desktop and mobile devices.
- **6.2** Players can install the application on supported devices as a Progressive Web App (PWA).
- **6.3** Players can access previously cached application resources when offline, where supported.

## Constraints

- The application is a web application, not a native iOS or Android application.
- The interface must be responsive and usable on small mobile screens.
- The application must work without user registration or login.
- Champion and item information must come from Riot Data Dragon.
- Item recommendations and counterpick suggestions must be based on predefined rules and curated data, not generative AI.
- The application must not require a custom backend or database.
- Saved builds must remain in the user's browser and must not be synchronized between devices.
- Shared build URLs must contain sufficient information to restore the shared selection without requiring an account.
- Offline functionality is limited to previously cached resources and data; live data cannot be guaranteed without an internet connection.
- The application must not collect unnecessary personal information.

## Out of Scope

The following features are intentionally excluded from the initial version:

- Native iOS and Android applications.
- Automatic champion recognition from images or screenshots.
- Live match detection or real-time game analysis.
- Live win-rate statistics and performance predictions.
- User accounts, authentication, and cloud synchronization.
- A backend server or database.
- Generative AI for creating builds or recommendations.
- Voice control, Siri integration, widgets, and haptic feedback.
- Push notifications about game patches.
- Social profiles, comments, and community features.


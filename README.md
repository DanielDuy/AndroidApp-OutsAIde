# AndroidApp-OutsAIde
An Android app that suggests outdoor activities based on weather data, location and your preferences - powered by artifical intelligence (OpenAI via Azure deployment). This was a project in one of our subjects in university and therefore will not provide the source code. But more down I show a demo use of the app we made.

## Features
- Shows weather data and sunrise time from MET (Meteorologisk institutt) API
- Uses OpenAI (gpt-4o via Azure) to suggests activities based on:
  - Time, location, number of people, distance, type of activity
- Integration with Google Places for location selection
- Displays hazard warnings and weather forecasts for the day
- Dark mode, choice of personal name via DataStore (key preferences)
- Save favorite search choices locally via Room Database

## Tools and frameworks
- Kotlin - Jetpack Compose
- MVVM architecture
- Hilt (dependency injection)
- Room and DataStore for storage
- OpenAI (Azure API)
- MET (weather, sunrise&sunset and warings) API
- Google places API

## What I did:
- Most of the backend development:
  - Setup of file structure
  - Viewmodels
  - Repositories
  - DataSources
  - Azure deployment and OpenAI API implementation and their following functions in the app
  - LocationForecast and sunrise&sunset API implementation from MET, deserilizing the JSON and their following functions in the app
  - Room and DataStore (Key Preferences) Database and their following functions in the app
  - Google Places API setup and implementation, and their following Jetpack compose dropdown menu and selection
  - Bug and crash fixes
  - Error handling
  - Tests

## Demonstration
![Demonstrasjon](appDemo_mainFunctionality.gif)
![Favorites og Google Maps](appDemo_changingSearchDetails_fromFavoritesDatabase.gif)
![Settings](appDemo_appSettings.gif)

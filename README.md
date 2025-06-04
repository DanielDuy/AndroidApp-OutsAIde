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

| Bibliotek                                                       | Forklaring for hvorfor vi brukte det              |
|-----------------------------------------------------------------|---------------------------------------------------|
| com.google.dagger:hilt-android                                  | Dependency injection-rammeverk                    |
| com.google.dagger:hilt-android-compiler                         | Kodegenerering for Hilt                           |
| androidx.hilt:hilt-navigation-compose                           | Hilt-integrasjon for Compose-navigasjon           |
| androidx.room:room-runtime                                      | Lokal database (Room) for lagring av sok          |
| androidx.datastore:datastore-preferences                        | Lokal database (key preferences) for instillinger |
| io.coil-kt:coil-gif                                             | Støtte for GIF-filer                              |
| com.google.android.libraries.places:places                      | Brukt til stedsøking i Norge                      |
| com.google.android.libraries.mapsplatform.secrets-gradle-plugin | Brukte til å håndtere hemmelige API nøkler        |
| com.azure:azure-ai-openai                                       | Tilgang til Azure OpenAI API                      |
| org.slf4j:slf4j-simple                                          | Logger for Azure SDK-er                           |
| androidx.test.espresso:espresso-core                            | UI-testing                                        |
| com.squareup.okhttp3:mockwebserver                              | Mock-server for å teste nettverkskall             |
| io.mockk:mockk                                                  | Mocking i Kotlin-tester                           |
| io.mockk:mockk-agent-jvm                                        | Agent for avansert mocking                        |
| io.noties.markwon:core                                          | Viser markdown-tekst i Compose                    |
| io.noties.markwon:syntax-highlight                              | Fargelegging av kode i markdown                   |

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

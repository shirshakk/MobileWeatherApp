## Overview
The Weather App is a Flutter application that fetches and displays the current weather information for a specified city using the OpenWeather API.

## Project Structure
```
.gitignore
.idea/
.metadata
analysis_options.yaml
android/
lib/
pubspec.lock
pubspec.yaml
README.md
test/
weather_app.iml
```

### Key Files and Directories
- **lib/main.dart**: The main entry point of the application.
- **lib/consts.dart**: Contains constants used in the application.
- **android/**: Contains Android-specific configuration and code.
- **test/**: Contains test files for the application.
- **pubspec.yaml**: Defines the dependencies and metadata for the project.

## Dependencies
The project uses the following dependencies:
- `flutter`: The Flutter SDK.
- `cupertino_icons`: Cupertino icons for iOS.
- `weather`: A package to fetch weather data.
- `intl`: A package for internationalization and localization.

## Getting Started
1. **Clone the repository**:
   ```sh
   git clone <repository-url>
   ```
2. **Navigate to the project directory**:
   ```sh
   cd weather_app
   ```
3. **Install dependencies**:
   ```sh
   flutter pub get
   ```
4. **Run the application**:
   ```sh
   flutter run
   ```

## Main Components
### main.dart
- **MyApp**: The root widget of the application.
- **HomePage**: The main screen displaying weather information.
- **_HomePageState**: The state class for `HomePage` that fetches and displays weather data.

### consts.dart
- **OPENWEATHER_API_KEY**: The API key for accessing the OpenWeather API.

## Weather Data Fetching
The weather data is fetched using the `WeatherFactory` class from the `weather` package. The API key is stored in consts.dart.

### Example:
```dart
final WeatherFactory _wf = WeatherFactory(OPENWEATHER_API_KEY);
_wf.currentWeatherByCityName("Delhi").then((w) {
  setState(() {
    _weather = w;
  });
});
```


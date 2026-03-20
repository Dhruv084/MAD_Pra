# Flutter Demo App

A Flutter application demonstrating ListView and Data Transfer between screens.

## Features

### Part A: ListView App
- Displays a list of 10 items using `ListView.builder`
- Shows Snackbar on item tap with message "You clicked Item X"
- Navigates to detail screen showing selected item

### Part B: Data Transfer Between Screens
- Two TextFields for user input (Name and Email)
- Input validation with error Snackbar
- Data transfer using Navigator and constructor
- Displays received data on SecondScreen

## Getting Started

### Prerequisites
- Flutter SDK installed
- Chrome browser (for web) or Android emulator

### Run the app
```bash
flutter pub get
flutter run -d chrome
```

## Project Structure
```
lib/
  └── main.dart    # Complete application code
```

## Technologies Used
- Flutter 3.x
- Dart
- Material Design 3

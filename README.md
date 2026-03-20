# 📱 Flutter Demo App - ListView & Data Transfer

A complete Flutter application demonstrating two essential Android/Flutter concepts: **ListView with dynamic data binding** and **Data Transfer between screens**.

---

## 📋 Table of Contents
- [Features](#features)
- [Screenshots](#screenshots)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [How It Works](#how-it-works)

---

## ✨ Features

### 🔹 Part A: ListView App
- Display a list of **10 unique items** using `ListView.builder`
- Dynamic data binding from a Dart List (array)
- **User Interaction**: Tap on any item to:
  - Show a **Snackbar** with message "You clicked Item X"
  - Navigate to a **Detail Screen** showing selected item
- Clean Card-based UI with CircleAvatar numbering

### 🔹 Part B: Data Transfer Between Screens
- **MainScreen** with two TextFields:
  - Name input field
  - Email input field
- **Input Validation**: Shows error Snackbar if fields are empty
- **Navigation**: Uses `Navigator.push` to transfer data
- **SecondScreen**: Displays received data in styled Cards
- Back button navigation to return to MainScreen

---

## 🗂️ Project Structure

```
MAD_PRA/
├── lib/
│   └── main.dart          # Complete application code (single file)
├── pubspec.yaml           # Flutter dependencies
├── pubspec.lock           # Locked dependency versions
├── .gitignore             # Git ignore rules
└── README.md              # Project documentation
```

---

## 🚀 Installation

### Prerequisites
- [Flutter SDK](https://flutter.dev/docs/get-started/install) (3.0 or higher)
- Chrome browser (for web) or Android Emulator

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/MAD_PRA.git
   cd MAD_PRA
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run -d chrome    # For web
   flutter run              # For connected device/emulator
   ```

---

## 📖 Usage

### Home Screen
- Two buttons to navigate to each module:
  - **Part A: ListView App** - Blue button
  - **Part B: Data Transfer** - Green button

### ListView App (Part A)
1. View the list of 10 items
2. Tap on any item to see Snackbar notification
3. Automatically navigates to Detail Screen
4. Press "Go Back" to return to list

### Data Transfer (Part B)
1. Enter your Name and Email
2. Press "Send Data" button
3. If fields are empty, error Snackbar appears
4. If valid, navigates to Second Screen with your data
5. Press "Go Back" to return

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| Flutter | UI Framework |
| Dart | Programming Language |
| Material Design 3 | UI Components |
| Navigator | Screen Navigation |
| ScaffoldMessenger | Snackbar Display |

---

## 💡 How It Works

### ListView Implementation
```dart
ListView.builder(
  itemCount: items.length,
  itemBuilder: (context, index) {
    return ListTile(
      title: Text(items[index]),
      onTap: () => // Handle tap
    );
  },
)
```

### Data Transfer via Constructor
```dart
// Sending data
Navigator.push(
  context,
  MaterialPageRoute(
    builder: (context) => SecondScreen(name: name, email: email),
  ),
);

// Receiving data
class SecondScreen extends StatelessWidget {
  final String name;
  final String email;
  
  const SecondScreen({required this.name, required this.email});
}
```

### Input Validation
```dart
if (name.isEmpty || email.isEmpty) {
  ScaffoldMessenger.of(context).showSnackBar(
    SnackBar(content: Text('Please fill in all fields!')),
  );
  return;
}
```

---

## 👨‍💻 Author

**Your Name**

---

## 📄 License

This project is for educational purposes (Mobile Application Development Practical).

---

⭐ **Star this repo if you found it helpful!**

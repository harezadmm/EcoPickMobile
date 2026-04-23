# 🌱 EcoPickMobile

**Eco-Friendly Waste Management Mobile Application**

A comprehensive mobile application designed to promote sustainable waste management practices through an innovative eco-system. EcoPickMobile empowers users to participate in waste reduction by reporting and collecting recyclable materials while earning eco-points.

![Flutter](https://img.shields.io/badge/Flutter-3.x-blue?style=flat-square&logo=flutter)
![Dart](https://img.shields.io/badge/Dart-3.x-blue?style=flat-square&logo=dart)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-Android%20|%20iOS%20|%20Web%20|%20Desktop-brightgreen?style=flat-square)

---

## 📋 Table of Contents

- [Features](#-features)
- [System Requirements](#-system-requirements)
- [Installation](#-installation)
  - [Windows Installation](#windows-installation)
  - [macOS Installation](#macos-installation)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Architecture](#-architecture)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

### 🔐 Authentication Module
- User registration with email verification
- Secure login system
- Password recovery and reset functionality
- Session management and auto-logout
- Social login integration ready

### 🏠 Home Screen
- Personalized dashboard with user statistics
- Quick access buttons to main features
- Activity summary and overview
- Real-time notifications

### 👤 Profile Management
- Complete user profile with avatar support
- Edit personal information
- Account settings and preferences
- Privacy and security controls
- Notification preferences

### 🗑️ EcoDrop Feature
- Report waste drop locations
- Google Maps integration for precise location marking
- Photo attachment for waste documentation
- Drop history and statistics
- Location-based waste tracking

### ♻️ EcoPick Feature
- Discover and pick waste from designated collection points
- Real-time location tracking
- Waste category identification
- Leaderboard for top contributors
- Achievement badges and milestones

### 💰 Wallet & Points System
- Accumulate eco-points from activities
- Digital wallet for earned rewards
- Points-to-cash conversion options
- Transaction history and receipts
- Referral bonus system
- Points expiry tracking

### 📊 Status Tracking
- Real-time activity monitoring
- Task progress visualization
- Historical data and analytics
- Monthly reports and insights
- Performance metrics dashboard

### 🛡️ Admin Module
- Comprehensive admin dashboard
- User account management
- Activity moderation and verification
- System monitoring and analytics
- Report generation tools
- Content management

### 🎨 UI/UX Design
- Modern Material Design interface
- Dark and Light theme support
- Responsive design for all screen sizes
- Smooth animations and transitions
- Accessibility features
- Localization support

### 🔧 Core Infrastructure
- Clean Architecture implementation
- Separation of concerns (Presentation, Domain, Data)
- Feature-based modular structure
- Service layer for business logic
- Utility functions and helpers
- State management solution

---

## 📱 System Requirements

### Common Requirements
- **Flutter SDK**: 3.0.0 or higher
- **Dart SDK**: 3.0.0 or higher
- **Internet Connection**: Required for full functionality
- **RAM**: Minimum 4GB (8GB recommended)
- **Storage**: 500MB free space

### Windows Requirements
- **OS**: Windows 10/11 (64-bit)
- **Visual Studio**: 2019 or later with C++ workload
- **Android SDK**: API level 21 or higher
- **Java Development Kit (JDK)**: 11 or higher

### macOS Requirements
- **OS**: macOS 10.15 (Catalina) or higher
- **Xcode**: 12.0 or later
- **CocoaPods**: 1.10.0 or higher
- **iOS Deployment Target**: 11.0 or higher

---

## 🚀 Installation

### Windows Installation

#### Prerequisites Installation

**1. Install Flutter SDK**
```bash
# Download Flutter SDK for Windows from:
# https://flutter.dev/docs/get-started/install/windows

# Extract to a folder (recommended: C:\src\flutter)
# Add Flutter to PATH:
# 1. Press Win + X, select "System"
# 2. Click "Advanced system settings"
# 3. Click "Environment Variables"
# 4. Add C:\src\flutter\bin to PATH
# 5. Restart terminal

# Verify installation
flutter --version
```

**2. Install Visual Studio**
```bash
# Download Visual Studio Community Edition:
# https://visualstudio.microsoft.com/vs/community/

# During installation, select:
# - Desktop development with C++
# - Windows 10/11 SDK
```

**3. Install Android SDK**
```bash
# Accept Android SDK licenses
flutter doctor --android-licenses
```

**4. Verify setup**
```bash
flutter doctor
```

#### Clone and Setup Project

```bash
# Clone the repository
git clone https://github.com/BlindCr/EcoPickMobile.git
cd EcoPickMobile

# Get dependencies
flutter pub get

# Generate generated files (if any)
flutter pub run build_runner build

# Check setup
flutter doctor
```

#### Run Application

```bash
# List available devices
flutter devices

# Run on Android emulator
flutter run -d <device_id>

# Run on Android device (with USB debugging enabled)
flutter run

# Run in release mode
flutter run --release
```

---

### macOS Installation

#### Prerequisites Installation

**1. Install Flutter SDK**
```bash
# Download Flutter SDK for macOS from:
# https://flutter.dev/docs/get-started/install/macos

# Extract to a folder (recommended: ~/development/flutter)
export PATH="$PATH:~/development/flutter/bin"

# Add to ~/.zprofile or ~/.bash_profile for permanent access
echo 'export PATH="$PATH:~/development/flutter/bin"' >> ~/.zprofile

# Verify installation
flutter --version
```

**2. Install Xcode**
```bash
# Install from App Store or:
xcode-select --install

# Accept Xcode license
sudo xcode-select --switch /Applications/Xcode.app/Contents/Developer

# Install Xcode build tools
sudo xcode-select --reset
```

**3. Install CocoaPods**
```bash
# Install CocoaPods
sudo gem install cocoapods

# Verify installation
pod --version
```

**4. Verify setup**
```bash
flutter doctor
```

#### Clone and Setup Project

```bash
# Clone the repository
git clone https://github.com/BlindCr/EcoPickMobile.git
cd EcoPickMobile

# Get dependencies
flutter pub get

# Generate generated files (if any)
flutter pub run build_runner build

# Check setup
flutter doctor
```

#### Run Application

```bash
# List available devices
flutter devices

# Run on iOS simulator
open -a Simulator
flutter run

# Run on physical iOS device
flutter run

# Run in release mode
flutter run --release
```

---

## 🎯 Getting Started

After installation, follow these steps:

### 1. Configure Firebase (Optional)
```bash
# If using Firebase features:
flutterfire configure
```

### 2. Set Environment Variables
Create a `.env` file in the root directory:
```
API_BASE_URL=https://your-api.com
API_KEY=your_api_key
ENVIRONMENT=development
```

### 3. Run Tests
```bash
# Run all tests
flutter test

# Run tests with coverage
flutter test --coverage
```

### 4. Build APK (Android)
```bash
# Build debug APK
flutter build apk

# Build release APK
flutter build apk --release

# Build app bundle
flutter build appbundle
```

### 5. Build IPA (iOS)
```bash
# Build for iOS
flutter build ios

# Build iOS app for distribution
flutter build ios --release
```

---

## 📁 Project Structure

```
lib/
├── core/                  # Core functionality (shared across features)
│   ├── services/         # API services, local storage
│   ├── utils/            # Helper functions and constants
│   └── theme/            # App theme configuration
│
├── features/             # Feature modules (Clean Architecture)
│   ├── admin/           # Admin dashboard and management
│   │   ├── presentation/
│   │   ├── domain/
│   │   └── data/
│   ├── auth/            # Authentication module
│   ├── ecodrop/         # EcoDrop feature
│   ├── ecopick/         # EcoPick feature
│   ├── home/            # Home screen
│   ├── profile/         # User profile
│   ├── status/          # Status tracking
│   └── wallet/          # Wallet & points system
│
├── navigation/          # App navigation and routing
├── main.dart           # App entry point
└── .env                # Environment variables
```

---

## 🏗️ Architecture

This project follows **Clean Architecture** principles with the following layers:

### Presentation Layer
- UI screens and widgets
- State management
- User interaction handling

### Domain Layer
- Business logic and use cases
- Entity definitions
- Repository interfaces

### Data Layer
- Repository implementations
- Data sources (API, Local DB)
- Data models and mappers

### Benefits
- ✅ Testability
- ✅ Maintainability
- ✅ Scalability
- ✅ Separation of concerns
- ✅ Easy feature addition

---

## 🛠️ Development Tools

### Code Generation
```bash
# Generate code from annotations
flutter pub run build_runner build --delete-conflicting-outputs
```

### Code Formatting
```bash
# Format code
dart format .

# Analyze code
dart analyze
```

### Debugging
```bash
# Enable verbose logging
flutter run -v

# Dart DevTools
flutter pub global activate devtools
devtools
```

---

## 📚 Dependencies

Key packages used:
- **flutter**: UI framework
- **provider**: State management
- **get_it**: Service locator
- **http**: HTTP client
- **shared_preferences**: Local storage
- **google_maps_flutter**: Maps integration
- **image_picker**: Image selection
- **permission_handler**: Permission management
- **intl**: Internationalization

See `pubspec.yaml` for complete list.

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style
- Follow Dart conventions
- Use meaningful variable names
- Add documentation comments
- Write unit tests for new features

---

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 📞 Support

For support and questions:
- 📧 Email: harizadhim760@gmail.com
- 🐛 Report issues: [GitHub Issues](https://github.com/BlindCr/EcoPickMobile/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/BlindCr/EcoPickMobile/discussions)

---

## 🙏 Acknowledgments

- Flutter and Dart community
- Contributors and testers
- Icons and assets providers

---

**Made with ♻️ for a sustainable future**

---

*Last updated: April 2026*

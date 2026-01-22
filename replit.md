# replit.md

## Overview

Prince Lite (Lite++) is a native Android application that provides a lightweight, specialized browser exclusively for Facebook. The app is built using Kotlin/Java with the Android SDK and focuses on offering enhanced features like token/cookie extraction, cookie editing, and desktop mode browsing.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Application Structure
- **Platform**: Native Android application (minimum SDK 24, target SDK 34)
- **Language**: Kotlin/Java hybrid
- **Build System**: Gradle with Android Gradle Plugin 8.13.1
- **UI Framework**: Material Design 3 (Material Components 1.13.0)

### Core Components
1. **WebView-based Browser**: Core functionality uses Android WebView to render Facebook pages with custom configurations
2. **Application Class**: Custom `App` class at `com.pronce.lite.app.App` for application-level initialization
3. **Single Activity Architecture**: Main activity handles Facebook browsing with feature toggles

### UI Architecture
- Material Design 3 theming with full light/dark mode support
- ConstraintLayout for responsive layouts
- Preference library for settings screens
- Custom drawable resources for app icons

### Key Features Implementation
- **Cookie Management**: Multi-format cookie support (String, Netscape, JSON Array, JSON Dictionary) with conversion capabilities
- **Token Extraction**: Access token retrieval from Facebook sessions
- **User Agent Switching**: Toggle between mobile and desktop browsing modes
- **In-app Updates**: Version checking via `updates.json` hosted on GitHub

### AndroidX Dependencies
- AppCompat 1.7.0
- Core KTX 1.13.0
- Fragment KTX 1.3.6
- Lifecycle components 2.6.2
- Preference 1.2.1
- Activity KTX 1.8.0

## External Dependencies

### Third-Party Libraries
- **Google Material Components 1.13.0**: UI components and theming
- **AndroidX Libraries**: Core Android Jetpack components for modern Android development

### Network Requirements
- Internet permission for Facebook access
- Network state permission for connectivity checks

### Update Mechanism
- Remote version checking via GitHub-hosted `updates.json`
- APK distribution through GitHub Releases

### No Backend Services
- This is a client-only application with no custom backend
- All data storage is local (SharedPreferences, WebView cookies)
- Updates and releases hosted on GitHub
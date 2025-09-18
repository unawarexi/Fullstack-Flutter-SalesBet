# SalesBet - No-Loss Betting Flutter App


## 📱 Screenshots

### Main Interface
<img width="885" height="1797" alt="Main App Interface" src="https://github.com/user-attachments/assets/d7f15e68-e154-4c4a-a024-70ada4f281b7" />

### Additional Views
<table>
  <tr>
    <td width="33%">
      <img width="100%" alt="Dashboard View" src="https://github.com/user-attachments/assets/84a0541a-11ab-4702-8a51-d1038e0571c8" />
    </td>
    <td width="33%">
      <img width="100%" alt="Betting Interface" src="https://github.com/user-attachments/assets/26637c68-a611-4501-b9fa-b5676e1ec196" />
    </td>
    <td width="33%">
      <img width="100%" alt="Profile & Settings" src="https://github.com/user-attachments/assets/d9d8ec6a-433b-42c2-8e3e-949f40231114" />
    </td>
  </tr>
</table>

## Core Concept - "No-Loss Betting"

### The Revolutionary Mechanic
Unlike traditional gambling apps, SalesBet introduces a risk-free betting system where users never lose credits — they only gain rewards when their predictions are correct.

### How It Works
1. **Stake Credits** → Credits are temporarily locked but never deducted
2. **Team Wins** → User's wallet increases with reward credits
3. **Team Loses** → Locked credits are simply released back to the user

### Key Advantages
- Removes gambling stigma and addiction risks
- Encourages frequent participation without fear
- Transforms credits into a gamified XP/loyalty system
- Promotes responsible engagement with sports predictions

## Architecture Overview

### Clean Architecture Implementation
- **UI Layer** → Widgets, screens, animations, and user interactions
- **State Management** → Riverpod for reactive business logic and app state
- **Repository Layer** → Firebase services abstraction (Auth, Firestore, Storage)
- **Domain Models** → User, Team, Event, Bet, Wallet entities
- **Security** → Backend enforcement via Firestore security rules and transaction logs

## Technology Stack & Libraries

### Authentication & Security
| Package | Purpose | Use Case |
|---------|---------|----------|
| `firebase_auth` | User authentication | Login, registration, session management |
| `google_sign_in` | OAuth integration | Quick Google account login |
| `github_sign_in_plus` | Developer login | GitHub OAuth for dev users |
| `pin_code_fields` | Security verification | PIN/OTP input interfaces |
| `local_auth` | Biometric auth | Fingerprint/Face ID verification |
| `flutter_secure_storage` | Encrypted storage | Sensitive data protection |

### Data & Storage
| Package | Purpose | Use Case |
|---------|---------|----------|
| `firebase_core` | Firebase foundation | Core Firebase initialization |
| `cloud_firestore` | NoSQL database | Real-time data sync, betting records |
| `firebase_storage` | File storage | User avatars, team logos, media |
| `shared_preferences` | Local preferences | User settings, app preferences |
| `get_storage` | High-performance storage | Cache management, offline data |

### Media & File Handling
| Package | Purpose | Use Case |
|---------|---------|----------|
| `image_picker` | Camera/gallery access | Profile pictures, content sharing |
| `file_picker` | Document selection | File uploads, document verification |

### Networking & Communication
| Package | Purpose | Use Case |
|---------|---------|----------|
| `http` | Basic HTTP requests | Simple API calls |
| `dio` | Advanced HTTP client | Complex API interactions, interceptors |
| `dio_smart_retry` | Request resilience | Automatic retry logic for failed requests |
| `socket_io_client` | Real-time communication | Live betting updates, chat features |
| `connectivity_plus` | Network monitoring | Offline/online state detection |

### UI Components & Visualization
| Package | Purpose | Use Case |
|---------|---------|----------|
| `fl_chart` | Data visualization | Betting statistics, performance charts |
| `carousel_slider` | Interactive sliders | Featured games, promotional content |
| `percent_indicator` | Progress visualization | Betting progress, completion status |
| `smooth_page_indicator` | Page navigation | Onboarding flow indicators |

### User Experience
| Package | Purpose | Use Case |
|---------|---------|----------|
| `iconsax` | Modern iconography | Consistent UI icons throughout app |
| `cupertino_icons` | iOS-style icons | Cross-platform icon consistency |
| `animated_splash_screen` | App launch experience | Branded loading experience |
| `page_transition` | Screen transitions | Smooth navigation animations |
| `flutter_spinkit` | Loading indicators | Various loading states |
| `status_alert` | User feedback | Success/error message displays |


### Notifications & Alerts
| Package | Purpose | Use Case |
|---------|---------|----------|
| `firebase_messaging` | Push notifications | Live score updates, betting reminders |
| `flutter_local_notifications` | Local alerts | Scheduled reminders, offline notifications |
| `fluttertoast` | Quick feedback | Simple success/error messages |

### Navigation & State
| Package | Purpose | Use Case |
|---------|---------|----------|
| `go_router` | Declarative routing | Type-safe navigation, deep linking |
| `flutter_riverpod` | State management | Reactive state, dependency injection |
| `get` | Utility functions | Quick utilities and helpers |

### Utilities & Tools
| Package | Purpose | Use Case |
|---------|---------|----------|
| `intl` | Internationalization | Date formatting, localization |
| `logger` | Development logging | Debugging and error tracking |
| `uuid` | Unique identifiers | Transaction IDs, unique keys |
| `url_launcher` | External links | Social media, external websites |
| `permission_handler` | Device permissions | Camera, location, notification access |
| `wakelock_plus` | Screen management | Keep screen on during live events |

## 🎮 Key Features

### Core Functionality
- **Risk-Free Betting System** - Revolutionary no-loss betting mechanic
- **Real-Time Updates** - Live score tracking and instant notifications
- **Social Integration** - Community features and leaderboards
- **Secure Wallet System** - Credit management without financial risk
- **Live Streaming Integration** - Watch games while betting

### User Experience
- **Dark Theme UI** - Gaming-focused design with neon accents
- **Interactive Onboarding** - Explains the unique "win-only" betting system
- **Celebration Animations** - Confetti and fireworks for winning predictions
- **Intuitive Navigation** - Home | Teams | Live Stream | Profile

## 🚀 Future Enhancements

### Phase 2 Features
- **Advanced Analytics** - Comprehensive betting performance dashboards
- **Enhanced Social Features** - Real-time chat rooms and community discussions
- **Scalable Streaming** - Integration with Agora/Twilio for live broadcasts
- **Smart Notifications** - AI-powered alerts for optimal betting opportunities
- **Rewards Marketplace** - Exchange credits for exclusive perks and merchandise

### Technical Improvements
- **Performance Optimization** - Advanced caching and data synchronization
- **Accessibility Features** - Enhanced support for users with disabilities
- **Multi-language Support** - Localization for global audience
- **Advanced Security** - Enhanced fraud detection and prevention

## 🎯 Getting Started

### Prerequisites
- Flutter SDK (^3.8.0)
- Firebase project setup
- Android Studio / VS Code
- Firebase CLI tools

### Installation
1. Clone the repository
2. Run `flutter pub get` to install dependencies
3. Configure Firebase for your project
4. Set up environment variables using `.env` file
5. Run the app using `flutter run`

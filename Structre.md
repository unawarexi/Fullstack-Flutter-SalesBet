

# architecture workflow
+---------------------------------------------------+
|                    Flutter App                    |
|  - UI (Home, Teams, Betting, Live Stream)         |
|  - State Mgmt (Riverpod/Bloc)                     |
|  - Firebase SDK (Auth, Firestore, Storage, FCM)   |
+---------------------------------------------------+

+-------------------+      +------------------------+
| Firebase Auth     |      | Firebase Firestore     |
| - Email/Social    |<---> | - Users                |
| - JWT tokens      |      | - Teams & Events       |
+-------------------+      | - Bets & Wallets       |
                           +------------------------+

+-------------------+      +------------------------+
| Firebase Storage  |      | Firebase Cloud Msg.    |
| - Thumbnails      |      | - Push Notifications   |
| - Stream metadata |      | - Team updates         |
+-------------------+      +------------------------+

+---------------------------------------------------+
|               External Integrations               |
| - Live Streaming (Agora/Twilio/WebRTC)            |
| - Payment gateways (future, if rewards → cashout) |
+---------------------------------------------------+


# struture
lib/
 ├── main.dart                   # Entry point
 ├── app.dart                    # MaterialApp, routes, theme
 │
 ├── core/                       # Shared utilities & base classes
 │    ├── constants/
 │    │    ├── app_colors.dart
 │    │    ├── app_icons.dart
 │    │    ├── app_strings.dart
 │    │    └── app_styles.dart
 │    ├── errors/
 │    │    └── failure.dart      # Error handling abstraction
 │    ├── utils/
 │    │    ├── validators.dart   # Input validation (emails, etc.)
 │    │    ├── formatters.dart   # Date/number formatters
 │    │    └── logger.dart
 │    └── widgets/
 │         ├── app_button.dart   # Reusable buttons
 │         ├── app_text_field.dart
 │         └── loading_indicator.dart
 │
 ├── models/                     # Data models
 │    ├── user_model.dart
 │    ├── team_model.dart
 │    ├── event_model.dart
 │    ├── bet_model.dart
 │    └── wallet_model.dart
 │
 ├── services/                   # External integrations
 │    ├── firebase_auth_service.dart
 │    ├── firestore_service.dart
 │    ├── storage_service.dart
 │    ├── notification_service.dart   # FCM
 │    └── wallet_service.dart
 │
 ├── features/                   # Feature-based organization
 │    ├── auth/
 │    │    ├── data/
 │    │    │    └── auth_repository.dart
 │    │    ├── presentation/
 │    │    │    ├── login_screen.dart
 │    │    │    └── signup_screen.dart
 │    │    └── state/
 │    │         └── auth_provider.dart
 │    │
 │    ├── home/
 │    │    ├── data/
 │    │    │    └── home_repository.dart
 │    │    ├── presentation/
 │    │    │    ├── home_screen.dart
 │    │    │    └── widgets/
 │    │    │         ├── challenge_card.dart
 │    │    │         └── trending_team_list.dart
 │    │    └── state/
 │    │         └── home_provider.dart
 │    │
 │    ├── teams/
 │    │    ├── data/
 │    │    │    └── teams_repository.dart
 │    │    ├── presentation/
 │    │    │    ├── team_list_screen.dart
 │    │    │    ├── team_detail_screen.dart
 │    │    │    └── widgets/
 │    │    │         ├── team_card.dart
 │    │    │         └── leaderboard_widget.dart
 │    │    └── state/
 │    │         └── teams_provider.dart
 │    │
 │    ├── betting/
 │    │    ├── data/
 │    │    │    └── betting_repository.dart
 │    │    ├── presentation/
 │    │    │    ├── betting_screen.dart
 │    │    │    └── widgets/
 │    │    │         └── betting_widget.dart
 │    │    └── state/
 │    │         └── betting_provider.dart
 │    │
 │    ├── live_stream/
 │    │    ├── data/
 │    │    │    └── stream_repository.dart
 │    │    ├── presentation/
 │    │    │    ├── live_stream_screen.dart
 │    │    │    └── widgets/
 │    │    │         └── chat_overlay.dart
 │    │    └── state/
 │    │         └── stream_provider.dart
 │    │
 │    ├── profile/
 │    │    ├── data/
 │    │    │    └── profile_repository.dart
 │    │    ├── presentation/
 │    │    │    └── profile_screen.dart
 │    │    └── state/
 │    │         └── profile_provider.dart
 │    │
 │    └── onboarding/
 │         ├── presentation/
 │         │    └── onboarding_screen.dart
 │         └── widgets/
 │              └── walkthrough_page.dart
 │
 └── router/
      └── app_router.dart         # GoRouter / Navigator setup

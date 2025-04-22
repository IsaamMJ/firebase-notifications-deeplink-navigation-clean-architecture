# 🔔 Flutter FCM Deep Link Demo

A Flutter application demonstrating the integration of **Firebase Cloud Messaging (FCM)** with **deep linking**. This project shows how to receive push notifications and navigate directly to a **specific product screen** when the user taps a notification.

## 🚀 Features

- ✅ Firebase Cloud Messaging setup
- ✅ Local notifications using `flutter_local_notifications`
- ✅ Token generation and permission handling
- ✅ Foreground and background message handling
- ✅ Deep link navigation using GetX
- ✅ Clean and scalable folder structure

## 📦 Dependencies

- `firebase_core`
- `firebase_messaging`
- `flutter_local_notifications`
- `get`
- `hive`

## 🔧 Setup Instructions

1. **Clone the repo**

```bash
git clone https://github.com/your-username/flutter-fcm-deeplink-demo.git
cd flutter-fcm-deeplink-demo
```

2. **Install dependencies**

```bash
flutter pub get
```

3. **Firebase setup**
   - Add your `google-services.json` file to `android/app/`
   - Make sure Firebase is configured in your Firebase Console

4. **Run the app**

```bash
flutter run
```

## 🧪 How to Test

1. Build and run the app on a physical Android device (not emulator).
2. Copy the FCM token from the console.
3. Go to the **Firebase Console > Cloud Messaging**
4. Send a test message using the copied FCM token.
5. Tap the notification → it will open the specific product screen.

## 🧠 How It Works

- When the app receives a push notification, it checks the `data` payload.
- If the type is `product_view`, it reads the `productId`.
- The app navigates to the appropriate screen using GetX and shows product details.

## 📁 Project Structure

```
lib/
├── core/
│   └── services/
│       └── firebase_notification_service.dart
├── controller/
├── data/
├── presentation/
│   └── pages/
├── routes/
│   ├── app_pages.dart
│   └── app_routes.dart
└── main.dart

## 📌 Future Enhancements

- iOS support
- Notification tap analytics
- In-app messaging
- User-level FCM topic subscription

---

Made with ❤️ using Flutter & Firebase
```

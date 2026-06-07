![App Banner](https://github.com/sanjeevRae/MYfiles/blob/main/Untitled%20design%20(1).jpg)

# AutoMarket: Real‑time Deal Alert App

**AutoMarket** is a Flutter‑based mobile client that receives instant push notifications about newly listed mobile phones from Facebook Marketplace (Nepal).  
It works seamlessly with the AutoMarket backend – displaying deals with photos, price, location, and a direct link to the original listing.  
The app registers your device token to Firestore, so the backend knows exactly where to send alerts – even when the app is closed.

---

## Technologies

- **Framework**: Flutter (Dart)
- **Backend Services**: Firebase Firestore, Firebase Cloud Messaging (FCM)
- **Image Hosting**: Cloudinary (optimised URLs)
- **State Management**: StreamBuilder + real‑time Firestore listeners
- **Platforms**: Android (min SDK 23), iOS (13+)
- **Authentication** (optional): Gmail API / Firebase Auth

---

## Architecture Overview (Notification Flow)

![Notification Flow Diagram](https://placehold.co/800x400/png?text=Backend+%E2%86%92+FCM+%E2%86%92+Mobile+App)  
*Diagram: Backend → FCM → Mobile device → Firestore read*

1. Backend scraper finds a new deal → uploads image to Cloudinary  
2. Backend writes listing to Firestore (`listings` collection)  
3. Backend sends FCM message with **visible notification** payload  
4. Mobile app shows notification (even if terminated)  
5. On tap, app opens and reads fresh deal data from Firestore

---

## Objectives

- **Deliver instant, visible alerts** – users never miss a good deal, even when the app is closed  
- **Provide a clean deal feed** – real‑time Firestore sync with optimised Cloudinary images  
- **Simplify token management** – automatically register and update FCM tokens in Firestore for backend broadcasting

---

## Features

- 🔔 **Push notifications** – Android & iOS, appears on lock screen / notification shade  
- 📱 **Deal browser** – sorted by newest, with photo, price, location, and direct Marketplace link  
- 🔥 **Real‑time Firestore** – new deals appear instantly without manual refresh  
- 🖼️ **Cloudinary image optimisation** – fast loading even on slow networks  
- 🔄 **Auto token registration** – device FCM token saved to `devices` collection on launch  
- 🧹 **Expired deal cleanup** – deals older than 30 days are automatically hidden (backend removes them)  
- 🎯 **Filtered scope** – only iPhones (X to 16 Pro) and Android phones (Samsung, Pixel, OnePlus, etc.)

---

## Getting Started

### Prerequisites

- Flutter 3.22+ & Dart 3.4+
- Firebase project with Firestore, FCM enabled
- For iOS: Apple Developer account + physical device

### Setup

```bash
git clone https://github.com/your-org/automarket-flutter.git
cd automarket-flutter
flutter pub get

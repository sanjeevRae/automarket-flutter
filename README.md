<!-- Typing animation header – now for the app -->
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3500&pause=500&color=14B8A6&center=true&vCenter=true&width=500&lines=AutoMarket+Flutter+App;Real‑time+Deal+Alerts;Push+Notifications+%F0%9F%94%94;Firestore+%2B+Cloudinary" alt="Typing SVG" />
</p>

<!-- Badges row – shields.io, all stable -->
<p align="center">
  <img src="https://img.shields.io/github/stars/your-org/automarket-flutter?logo=github&style=for-the-badge&color=14b8a6&labelColor=0D1117" />
  <img src="https://img.shields.io/github/forks/your-org/automarket-flutter?logo=github&style=for-the-badge&color=14b8a6&labelColor=0D1117" />
  <img src="https://img.shields.io/github/issues/your-org/automarket-flutter?logo=github&style=for-the-badge&color=14b8a6&labelColor=0D1117" />
  <img src="https://img.shields.io/badge/Flutter-3.22+-02569B?style=for-the-badge&logo=flutter&logoColor=white&labelColor=0D1117" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black&labelColor=0D1117" />
</p>

---

## 📱 About The App

<p align="center">
  🔔 <strong>Push notifications</strong> for new mobile phone deals &nbsp;|&nbsp;
  🖼️ <strong>Cloudinary</strong> optimised images &nbsp;|&nbsp;
  🔥 <strong>Firestore</strong> real‑time feed
</p>

<p align="center">
  AutoMarket watches Facebook Marketplace for iPhone and Android listings in Nepal,<br />
  filters by keywords & price, and sends <strong>visible push notifications</strong> even when the app is closed.<br />
  This Flutter client displays the deals, registers your device token, and keeps you updated instantly.
</p>

<table align="center">
  <tr>
    <td>🚀 Key feature</th>
    <td>Backend delivers <code>notification</code> payload – no app launch required</th>
   </tr>
   <tr>
    <td>📦 Firestore collections</th>
    <td><code>listings</code> (deals) and <code>devices</code> (FCM tokens)</th>
   </tr>
   <tr>
    <td>🧹 Auto cleanup</th>
    <td>Expired deals (<code>expiresAt ≤ now</code>) vanish automatically</th>
   </tr>
   <tr>
    <td>🔗 Deep links</th>
    <td>Open original Facebook Marketplace listing with one tap</th>
   </tr>
</table>

> **Backend repo** – [AutoMarket Backend](https://github.com/your-org/automarket-backend) (scraper, Cloudinary upload, FCM sender)

---

## 🛠️ Tech Stack (Mobile)

<p align="center">
  <img src="https://skillicons.dev/icons?i=flutter,dart,firebase" />
</p>
<p align="center">
  <img src="https://skillicons.dev/icons?i=androidstudio,gradle,git" />
</p>
<p align="center">
  <i>Cloudinary for images • FCM for push • Firestore for real‑time data</i>
</p>

---

## 🚀 Getting Started

### Prerequisites

- Flutter 3.22+ (Dart 3.4+)
- Firebase project with Firestore, FCM, and Android/iOS apps added
- For iOS: Apple Developer account + physical device for push testing

### Installation

```bash
git clone https://github.com/your-org/automarket-flutter.git
cd automarket-flutter
flutter pub get

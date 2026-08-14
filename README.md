# 🎫 PassCheck By DM

<img width="150" height="150" alt="favicon" src="https://github.com/user-attachments/assets/43b37584-5543-45fc-9f44-9e8efde60c24" />


> A mobile-first, PWA-enabled QR Code Pass Generator, Sharing Engine, and Gatekeeper Scanner built in classic **iOS 6 Skeuomorphic** style.

[![PWA Ready](https://img.shields.io/badge/PWA-Enabled-blueviolet.svg)](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Theme](https://img.shields.io/badge/Theme-iOS_6_Skeuomorphic-blue.svg)](#-ui--design)
[![Dependencies](https://img.shields.io/badge/Dependencies-Zero_Build_Step-brightgreen.svg)](#-tech-stack)

https://passcheckbydm.netlify.app/

---

## 📌 Overview

**PassCheck** is a lightweight, web-based mobile application designed for event managers, hosts, and venue organizers. It allows you to quickly issue personalized, secure QR code pass tickets for attendees (including names, phone numbers, seating arrangements, and custom access levels), export/share them instantly, and use a second camera device as a quick-access **Gatekeeper Reader** with real-time visual and audio verification.

Styled with nostalgic **iOS 6 skeuomorphism**—complete with glossy aqua buttons, stitched leather header trims, metallic segmented tab bar controllers, and frosted glass HUD overlays.

---

## ✨ Key Features

### 1. 🎟️ Passbook Ticket & QR Generator
- Custom event configuration (Event Name, Attendee Name, Phone, Seat Number/Tier, Custom Gates).
- Unique auto-generated Ticket Hash ID to prevent basic ticket forgery.
- Embedded high-density QR code rendering on a physical-feeling glossy ticket card.

### 2. 📤 Pass Export & Web Sharing
- **Web Share API**: Native device sharing prompt for direct sending via WhatsApp, iMessage, Mail, or Telegram.
- **Image Export**: Download high-resolution PNG copies of generated ticket passes directly to device storage.
- **Payload Clipboard Copy**: One-tap copy of encoded ticket payload for database or SMS distribution.

### 3. 🔍 Gatekeeper Reader & Scanner
- **Live Camera Stream**: Fast, continuous real-time QR scanning powered by `jsQR`.
- **Camera Switcher & Flash Toggle**: Front/rear camera toggle with hardware flashlight support (where browser supported).
- **File Upload Fallback**: Scan ticket images directly from photo galleries or file storage.

### 4. 🛑 Instant Audio/Visual Verification
- **Visual Feedback HUD**: 
  - 🟩 **Green Checkmark Glass Overlay** for valid first-time access.
  - 🟥 **Red Warning Cross Glass Overlay** for double check-ins or invalid barcodes.
- **Web Audio API Sound Engine**: Synth audio feedback with positive access chimes or negative warning buzzers without external audio asset dependencies.
- **Local Scan Registry**: Tracks scanned ticket IDs to instantly flag duplicate entries.

### 5. 📱 Mobile-First PWA & Offline Support
- Built-in **Service Worker (`sw.js`)** for offline caching and instant boot-up times.
- Web App Manifest (`manifest.json`) for full-screen "Add to Home Screen" installation on iOS Safari and Android Chrome.

### 6. 🎨 iOS 6 Aesthetic & Themes
- **Light Mode Default**: Classic linen backdrop, silver navigation bars, and stitched leather accents.
- **Dark Skeuomorphism Toggle**: Dark carbon slate backdrops with illuminated metallic controls.

---

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, Modern ES6 JavaScript.
- **QR Generator**: `qrcode.js` (Canvas & SVG generation).
- **QR Scanner**: `jsQR` (Client-side camera stream processing).
- **Audio Engine**: Web Audio API (`AudioContext` synthesizers).
- **Storage**: Browser `localStorage` / `IndexedDB`.
- **PWA**: Service Worker (`sw.js`) + Web App Manifest (`manifest.json`).

---

## 📁 Repository Structure

```text
├── index.html          # Main application UI and logic
├── manifest.json       # Web App Manifest for mobile installation
├── sw.js               # Service Worker for offline asset caching
├── icons/              # App launcher icons (192x192, 512x512)
│   ├── icon-192.png
│   └── icon-512.png
└── README.md           # Repository documentation

```

---

## 🚀 Quick Start & Installation

Because **PassKeeper iOS 6** relies on zero build tools or npm package compilers, you can run it immediately with any static file web server.

### Option A: Local Static Server (Recommended)

Due to Web Camera security policies (`getUserMedia`), camera access requires **HTTPS** or `localhost`.

1. **Clone the repository:**
```bash
git clone [https://github.com/your-username/passkeeper-ios6.git](https://github.com/your-username/passkeeper-ios6.git)
cd passkeeper-ios6

```


2. **Serve using a simple local server:**
*Using Python 3:*
```bash
python -m http.server 8000

```


*Using Node `serve`:*
```bash
npx serve .

```


3. **Open in your browser:**
```text
http://localhost:8000

```



---

## 📲 Installing as a Progressive Web App (PWA)

### On iOS (Safari):

1. Open the application URL in Safari.
2. Tap the **Share** button at the bottom of the screen.
3. Scroll down and select **Add to Home Screen**.
4. Tap **Add**. The app will appear on your home screen with a standalone app window.

### On Android (Chrome):

1. Open the application URL in Chrome.
2. Tap the **Three Dots Menu** at the top right.
3. Tap **Install App** or **Add to Home Screen**.

---

## ⚠️ Camera Permissions & HTTPS Notice

Browsers restrict live camera access (`navigator.mediaDevices.getUserMedia`) to secure contexts.

* **Local Development**: Works out of the box on `http://localhost` or `http://127.0.0.1`.
* **Production Deployment**: You **must** host this app over **HTTPS** (e.g., GitHub Pages, Vercel, Netlify, or Cloudflare Pages) for the camera scanner to function on mobile devices.

---

## 📄 License

This project is open-source and available under the [MIT License](https://www.google.com/search?q=LICENSE).

---

## Screenshots

<img width="1901" height="915" alt="Screenshot 2026-08-12 215221" src="https://github.com/user-attachments/assets/e5c676c0-3e93-42b6-9511-adae31d195a7" />

<img width="1904" height="918" alt="Screenshot 2026-08-12 215200" src="https://github.com/user-attachments/assets/9c4bd5a8-da08-489b-93cb-40f74649d560" />

<img width="1903" height="917" alt="Screenshot 2026-08-12 215211" src="https://github.com/user-attachments/assets/308bc62d-9ca9-4919-9f46-3133b02e3381" />

<img width="1901" height="915" alt="Screenshot 2026-08-12 215231" src="https://github.com/user-attachments/assets/d2b376f8-13ef-49ad-ab48-0ab4bfdf5f4a" />

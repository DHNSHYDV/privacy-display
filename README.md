# Privacy Guard (Privacy Display)

[![Platform](https://img.shields.io/badge/Platform-Android%208.0%2B-green.svg)](https://developer.android.com)
[![Target](https://img.shields.io/badge/Target-Android%2015%20%7C%20One%20UI%207-blue.svg)](https://www.samsung.com/one-ui/)
[![Latest Release](https://img.shields.io/github/v/release/DHNSHYDV/privacy-display?color=blue&label=Latest%20Version)](https://github.com/DHNSHYDV/privacy-display/releases/latest)
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](LICENSE)

A smart, tilt-activated privacy screen utility for Android that automatically obscures your screen with **100% opaque, corner-to-corner frosted glass** whenever your phone is tilted away or viewed from side angles.

Engineered natively for **Samsung One UI 7 (Galaxy Note 10+)**, **Google Pixel**, and all modern Android devices.

---

## 📥 Downloads & Releases

Get the latest installable APKs directly from the **[Releases Page](https://github.com/DHNSHYDV/privacy-display/releases)**:

| Version | Download | Status | Highlights |
| :--- | :--- | :--- | :--- |
| **v1.1.0** | [**Download APK (v1.1.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.1.0/PrivacyGuard-v1.1.0.apk) | **Latest** | 6 randomized 4K frosted glass textures + 1-Tap Quick Settings panel addition |
| **v1.0.0** | [**Download APK (v1.0.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.0.0/PrivacyGuard-v1.0.apk) | Stable | Initial release with core tilt engine & One UI 7 QS tile |

---

## 🔒 Why Privacy Guard?

When commuting on crowded trains, metros, or reading sensitive personal chats and emails in public, people around you can easily peek at your screen. 

Traditional plastic "privacy screen protectors" degrade your display clarity, ruin viewing angles for you, and dim brightness. 

**Privacy Guard** solves this purely in software at the hardware compositor level:
* Add the **Privacy Guard** tile to your **Quick Settings** shade.
* Tap it once to enable protection.
* While you hold your phone straight (facing you), your display is completely normal with 100% native clarity and brightness.
* As soon as your phone tilts left or right past a set angle (e.g. $\pm 22^\circ$), the screen instantly covers corner-to-corner in **100% opaque frosted glass**, blocking any onlooker's view.
* Bring the phone upright again, and the screen instantly unlocks and clears!

---

## ✨ Features

* **One UI 7 & Pixel Quick Settings Tile**:
  * Toggled directly from the pull-down Quick Settings shade (`TileService`).
  * Shows real-time Active/Inactive status with dynamic subtitle indicators.
  * Includes a **1-Tap Quick Settings setup button** that triggers Android 13+ native tile addition without manual dragging.
* **100% Hardware-Level Opacity**:
  * Uses `PixelFormat.OPAQUE` via Android's `WindowManager` to completely eliminate GPU alpha blending.
  * Zero see-through, zero text bleed, and absolute privacy.
* **True Corner-to-Corner Fullscreen**:
  * Configured with `LAYOUT_IN_DISPLAY_CUTOUT_MODE_ALWAYS` and zero system insets (`fitInsetsTypes = 0`).
  * Extends completely over navigation bars, gesture handles, camera cutouts, and rounded corners.
* **6 Realistic 4K Frosted Glass Textures**:
  * Randomly alternates between 6 textures on each tilt activation:
    1. Smooth frosted ice gradient
    2. Condensation & rain streak window
    3. Deep etched dark glass with vignette
    4. Veined / crackled champagne frosted glass
    5. Metallic aqua / cyan textured plaster glass
    6. Soft pastel rainbow frosted grain blur
* **Low-Power Sensor Fusion Engine**:
  * High-precision Roll tracking using `Sensor.TYPE_ROTATION_VECTOR` with low-pass exponential smoothing ($\alpha = 0.25$) and hysteresis ($3.0^\circ$) to eliminate boundary flicker.
  * Includes an automatic mathematical fallback (`Sensor.TYPE_ACCELEROMETER` + trigonometry) for devices lacking a physical gyroscope.
* **Interactive Calibration Dashboard**:
  * Live spirit-level angle gauge showing real-time roll degrees.
  * Threshold sensitivity slider ($10^\circ$ to $45^\circ$).
  * Touch pass-through toggle (choose whether to allow taps through the frosted view or block accidental input).

---

## 📲 How to Install & Setup

1. **Download**: Download [**PrivacyGuard-v1.1.0.apk**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.1.0/PrivacyGuard-v1.1.0.apk) onto your phone.
2. **Install**: Tap the downloaded file to install. If prompted by Android, tap **"Allow from this source"** to enable sideloading.
3. **Grant Permission**: Open **Privacy Guard** and tap **"Grant Overlay Permission"** (toggle "Allow display over other apps").
4. **Add to Quick Settings**:
   * *Option A (Automatic)*: Tap **"Add to Quick Settings Panel"** inside the app $\to$ tap **Add** on the system prompt.
   * *Option B (Manual)*: Swipe down twice from the top of your screen $\to$ tap the **Edit (Pencil)** icon $\to$ drag **Privacy Guard** into your active tiles.
5. **Ready**: Tap the Quick Settings tile anytime you want protection on crowded transit or in public!

---

## 🛡️ Security & Privacy Guarantee

* **100% Offline**: Privacy Guard contains **no internet permission** (`android.permission.INTERNET` is omitted from the manifest).
* **Zero Telemetry**: No tracking, no analytics, no ads, and no data collection.
* **Open Distribution**: Clean standalone APK packages compiled directly from source.

---

## 💬 Issues & Feature Requests

Found a bug or have an idea for an awesome new frosted texture or feature? Feel free to open an issue in the **[Issues Tab](https://github.com/DHNSHYDV/privacy-display/issues)**!

---

## 📄 License

This distribution is released under the [MIT License](LICENSE).
Copyright (c) 2026 Dhanush Yadav (DHNSHYDV).

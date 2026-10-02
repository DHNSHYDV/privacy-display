# Privacy Guard (Privacy Display)

[![Platform](https://img.shields.io/badge/Platform-Android%208.0%2B-green.svg)](https://developer.android.com)
[![Target](https://img.shields.io/badge/Target-Android%2015%20%7C%20One%20UI%207-blue.svg)](https://www.samsung.com/one-ui/)
[![Latest Release](https://img.shields.io/github/v/release/DHNSHYDV/privacy-display?color=blue&label=Latest%20Version)](https://github.com/DHNSHYDV/privacy-display/releases/latest)
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](LICENSE)

A smart privacy screen utility for Android that automatically obscures your display with **100% opaque, corner-to-corner frosted glass** using **hardware tilt sensors** and **on-device selfie camera snooper detection** whenever someone looks over your shoulder or tilts your phone.

Engineered natively for **Samsung One UI 7 (Galaxy Note 10+)**, **Google Pixel**, and all modern Android devices.

---

## 📥 Downloads & Releases

Get the latest installable APKs directly from the **[Releases Page](https://github.com/DHNSHYDV/privacy-display/releases)**:

| Version | Download | Status | Highlights |
| :--- | :--- | :--- | :--- |
| **v1.2.0** | [**Download APK (v1.2.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.2.0/PrivacyGuard-v1.2.0.apk) | **Latest** | **On-Device Camera Snooper Guard** (Google ML Kit Face Detection) + Dual Trigger Controls |
| **v1.1.0** | [**Download APK (v1.1.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.1.0/PrivacyGuard-v1.1.0.apk) | Stable | 6 randomized 4K frosted glass textures + 1-Tap Quick Settings panel addition |
| **v1.0.0** | [**Download APK (v1.0.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.0.0/PrivacyGuard-v1.0.apk) | Stable | Initial release with core tilt engine & One UI 7 QS tile |

---

## 🔒 Dual-Layer Privacy Protection

Privacy Guard gives you two complementary, battle-tested privacy mechanisms:

```
+-------------------------------------------------------------------------+
|                              PRIVACY GUARD                              |
+------------------------------------+------------------------------------+
|         1. TILT WRIST FLICK        |      2. CAMERA SNOOPER GUARD       |
+------------------------------------+------------------------------------+
| Triggers when the phone moves past | Triggers when the front camera     |
| a set angle (e.g. ±22°).           | detects >1 face looking at screen. |
|                                    |                                    |
| • Instant reflex hide              | • Read normally while holding      |
| • No screen lock delay             |   phone straight at 0°             |
| • Anti-snatch protection           | • On-device Google ML Kit (offline)|
| • Zero battery consumption         | • Throttled at 2.5 FPS for low heat|
+------------------------------------+------------------------------------+
                                     |
                                     v
                 [ 100% OPAQUE FULL-BLEED FROSTED GLASS ]
                 - Covers navigation bar, cutout, & corners
                 - Randomizes across 6 realistic 4K textures
```

---

## ✨ Key Features

* **AI Snooper Guard (Google ML Kit Face Detection)**:
  * Reads the front camera in real time using a battery-optimized background pipeline (throttled to ~2.5 FPS).
  * If a bystander looks over your shoulder, the phone detects the secondary face and immediately covers your screen.
  * When the onlooker looks away or walks off, your screen unlocks instantly.
* **Panic Wrist-Flick (Hardware Tilt Sensor Fusion)**:
  * Uses high-precision `Sensor.TYPE_ROTATION_VECTOR` with low-pass exponential filtering and hysteresis.
  * Flick your wrist slightly away to hide your display without pressing power or locking yourself out.
* **One UI 7 & Pixel Quick Settings Tile**:
  * Toggled directly from the pull-down Quick Settings shade (`TileService`).
  * Includes a **1-Tap Quick Settings setup button** that triggers Android 13+ native tile addition without manual dragging.
* **100% Hardware-Level Opacity**:
  * Uses `PixelFormat.OPAQUE` via Android's `WindowManager` to completely eliminate GPU alpha blending.
  * Zero see-through, zero text bleed, and absolute privacy.
* **True Corner-to-Corner Fullscreen**:
  * Configured with `LAYOUT_IN_DISPLAY_CUTOUT_MODE_ALWAYS` and zero system insets (`fitInsetsTypes = 0`).
  * Extends completely over navigation bars, gesture handles, camera cutouts, and rounded corners.
* **6 Realistic 4K Frosted Glass Textures**:
  * Randomly alternates between 6 textures on each activation:
    1. Smooth frosted ice gradient
    2. Condensation & rain streak window
    3. Deep etched dark glass with vignette
    4. Veined / crackled champagne frosted glass
    5. Metallic aqua / cyan textured plaster glass
    6. Soft pastel rainbow frosted grain blur

---

## 📲 How to Install & Setup

1. **Download**: Download [**PrivacyGuard-v1.2.0.apk**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.2.0/PrivacyGuard-v1.2.0.apk) onto your phone.
2. **Install**: Tap the downloaded file to install. If prompted by Android, tap **"Allow from this source"** to enable sideloading.
3. **Grant Permissions**:
   * **Overlay Permission**: Tap "Grant Overlay Permission" (allow "Display over other apps").
   * **Camera Permission**: Tap "Grant Camera Permission" (used strictly on-device for snooper detection).
4. **Add to Quick Settings**:
   * Tap **"Add to Quick Settings Panel"** inside the app $\to$ tap **Add** on the system prompt.
5. **Ready**: Toggle Privacy Guard anytime from your Quick Settings!

---

## 🛡️ Security & Privacy Guarantee

* **100% Offline Processing**: Privacy Guard contains **no internet permission** (`android.permission.INTERNET` is omitted from the manifest).
* **Zero Video/Photo Recording**: The front camera frames are analyzed ephemerally in RAM (memory) to count face bounding boxes, and are **immediately discarded**. No photos or videos are ever written to phone storage.
* **Zero Telemetry**: No tracking, no analytics, no ads, and no data collection.

---

## 💬 Issues & Feature Requests

Found a bug or have an idea for an awesome new feature? Feel free to open an issue in the **[Issues Tab](https://github.com/DHNSHYDV/privacy-display/issues)**!

---

## 📄 License

This distribution is released under the [MIT License](LICENSE).
Copyright (c) 2026 Dhanush Yadav (DHNSHYDV).

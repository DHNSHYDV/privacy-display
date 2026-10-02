# Privacy Guard (Privacy Display)

[![Platform](https://img.shields.io/badge/Platform-Android%208.0%2B-green.svg)](https://developer.android.com)
[![Target](https://img.shields.io/badge/Target-Android%2015%20%7C%20One%20UI%207-blue.svg)](https://www.samsung.com/one-ui/)
[![Latest Release](https://img.shields.io/github/v/release/DHNSHYDV/privacy-display?color=blue&label=Latest%20Version)](https://github.com/DHNSHYDV/privacy-display/releases/latest)
[![License](https://img.shields.io/badge/License-MIT-orange.svg)](LICENSE)

A clean, autonomous privacy utility for Android that automatically obscures your display with **100% opaque, corner-to-corner frosted glass** whenever someone looks over your shoulder.

Engineered natively for **Samsung One UI 7 (Galaxy Note 10+)**, **Google Pixel**, and all modern Android devices.

---

## 📥 Downloads & Releases

Get the latest installable APKs directly from the **[Releases Page](https://github.com/DHNSHYDV/privacy-display/releases)**:

| Version | Download | Status | Highlights |
| :--- | :--- | :--- | :--- |
| **v1.4.0** | [**Download APK (v1.4.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.4.0/PrivacyGuard-v1.4.0.apk) | **Latest** | **Dark OLED Bento-Box UI Redesign** + New high-res frosted shield logo + Unified "Privacy Guard" branding |
| **v1.3.1** | [**Download APK (v1.3.1)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.3.1/PrivacyGuard-v1.3.1.apk) | Stable | Zero-Flicker QS Trampoline: Reliable background QS toggle on Android 14+ |
| **v1.3.0** | [**Download APK (v1.3.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.3.0/PrivacyGuard-v1.3.0.apk) | Stable | Pure Face Snooper Guard (removed tilt sensor) + Full Camera On/Off control from Quick Settings |
| **v1.2.0** | [**Download APK (v1.2.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.2.0/PrivacyGuard-v1.2.0.apk) | Stable | On-device Google ML Kit Face Detection pipeline |
| **v1.1.0** | [**Download APK (v1.1.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.1.0/PrivacyGuard-v1.1.0.apk) | Stable | 6 randomized 4K frosted glass textures + 1-Tap QS panel addition |
| **v1.0.0** | [**Download APK (v1.0.0)**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.0.0/PrivacyGuard-v1.0.apk) | Stable | Initial release |

---

## 🔒 How It Works (Privacy Guard)

No awkward wrist tilts or sensor gimmicks. You hold your phone naturally and read comfortably:

```
[ Quick Settings Shade ]  ---> Tap "Privacy Guard" Tile
                                          |
                              Camera turns ON in background
                                          |
                         (CameraX @ ~3 FPS, 360p Low-Power)
                                          |
                             Google ML Kit Face Detection
                                          |
                              Faces > 1 Detected?
                              /                 \
                           YES                   NO
                            |                     |
                            v                     v
                 [ Frosted Glass Active ]    [ Clear Screen ]
                 - 100% Opaque               - Read normally
                 - Covers nav bar & cutout   - Zero distortion
                 - Onlooker sees frosted ice
```

When you are done, tap the Quick Settings tile again: the service stops, the front camera immediately powers down, and the green dot disappears.

---

## ✨ Key Features

* **100% Autonomous Quick Settings Control**:
  * Tap the tile once $\to$ camera powers up and starts guarding.
  * Tap the tile again $\to$ camera powers down immediately and hardware is released.
  * You never need to open the app after granting initial permissions.
* **On-Device Google ML Kit Face Detection**:
  * Detects secondary onlookers glancing at your phone.
  * Throttled to ~3 FPS at 360p resolution for negligible battery and zero heating.
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

1. **Download**: Download [**PrivacyGuard-v1.4.0.apk**](https://github.com/DHNSHYDV/privacy-display/releases/download/v1.4.0/PrivacyGuard-v1.4.0.apk) onto your phone.
2. **Install**: Tap the downloaded file to install. If prompted by Android, tap **"Allow from this source"** to enable sideloading.
3. **Grant Permissions (One time only)**:
   * **Overlay Permission**: Tap "Grant Overlay Permission" (allow "Display over other apps").
   * **Camera Permission**: Tap "Grant Camera Permission" (used strictly on-device for face privacy protection).
4. **Add to Quick Settings**:
   * Tap **"Add Tile"** inside the app $\to$ tap **Add** on the system prompt.
5. **Control from QS Shade**: Pull down Quick Settings anytime to turn Privacy Guard ON or OFF!

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

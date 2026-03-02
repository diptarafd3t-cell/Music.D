# 🎵 Music.D — Premium YouTube Interface

A professional, ultra-modern YouTube video player interface featuring a cinematic **Glassmorphism** design. This single-page application (SPA) utilizes dynamic background animations and a robust URL parser to provide a premium viewing experience.

![Version](https://img.shields.io/badge/Version-1.1.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![UI-Style](https://img.shields.io/badge/Style-Glassmorphism-purple)
![Responsive](https://img.shields.io/badge/Mobile-Optimized-success)

---

## ✨ Key Features

* **Glassmorphism UI:** Implements `backdrop-filter: blur(25px)` and thin borders to create a high-end "frosted glass" effect.
* **Animated Ambient Background:** Features three dynamic "blobs" (Indigo, Pink, and Red) that use CSS Keyframes to drift and scale, mimicking an OLED-friendly ambient light experience.
* **Universal URL Parser:** An advanced Regular Expression (Regex) engine that extracts Video IDs from:
    * Standard Desktop URLs (`youtube.com/watch?v=...`)
    * Shortened Share Links (`youtu.be/...`)
    * **YouTube Shorts** (`youtube.com/shorts/...`)
    * Embed URLs and Tracking IDs.
* **Instant Interaction:** Supports "Enter" key submission and automatic title updating.

---

## 🚀 Execution Workflow



1.  **Capture:** User inputs any YouTube-related link.
2.  **Extract:** JavaScript Regex strips away parameters and identifies the 11-character ID.
3.  **Inject:** The DOM updates the `<iframe>` source dynamically.
4.  **Immerse:** The player reloads with the new content while maintaining the ambient background.

---

## 🛠️ Built With

* **HTML5:** Semantic structure with optimized meta tags for mobile.
* **CSS3 (Advanced):** * **Custom Variables:** For easy color-palette swapping.
    * **Keyframes:** Hardware-accelerated `transform` animations for 60fps movement.
    * **Flexbox:** Responsive centering and layout management.
* **Vanilla JavaScript:** * Regex-based validation.
    * Event listeners for seamless keyboard navigation.

---

## 🧪 Technical Details

The engine of the application is this resilient Regex string:

```javascript
const regex = /(?:youtube\.com\/(?:[^\/]+\/.+\/|(?:v|e(?:mbed)?|shorts)\/|.*[?&]v=)|youtu\.be\/)([^"&?\/\s]{11})/;

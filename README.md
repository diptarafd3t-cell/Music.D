# 🎵 Music.D — Premium YouTube Interface

A professional, ultra-modern YouTube video player interface featuring a cinematic **Glassmorphism** design. This single-page application uses dynamic background animations and a robust URL parser to provide a premium, distraction-free viewing experience.

![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![UI-Style](https://img.shields.io/badge/Style-Glassmorphism-purple)
![Tech](https://img.shields.io/badge/Tech-HTML5%20%7C%20CSS3%20%7C%20JS-orange)

---

## ✨ Key Features

* **Glassmorphism UI:** High-end aesthetic using `backdrop-filter: blur()` and semi-transparent borders for a "frosted glass" look.
* **Animated Ambient Background:** Three distinct "blobs" (Indigo, Pink, and Red) that drift and scale automatically to create a deep, immersive atmosphere.
* **Smart URL Parser:** An advanced Regular Expression (Regex) engine that extracts Video IDs from almost any YouTube format:
    * Standard Desktop (`youtube.com/watch?v=...`)
    * Shortened Mobile Links (`youtu.be/...`)
    * **YouTube Shorts** (`youtube.com/shorts/...`)
    * Embedded Links
* **Responsive Architecture:** Fully optimized for mobile, tablet, and desktop with a fluid 16:9 aspect ratio container.
* **Premium Typography:** Styled with *Plus Jakarta Sans* for a modern, tech-focused feel.

---

## 🚀 Quick Start

1.  **Clone or Copy:** Save the project code as `index.html`.
2.  **Launch:** Open the file in any modern browser (Chrome, Brave, Safari, Edge).
3.  **Usage:** * Copy a YouTube URL (e.g., `https://youtu.be/K8fBH3D8S-A`).
    * Paste it into the input field at the bottom.
    * Press **Enter** or click **"Load Video"**.

---

## 🛠️ Technical Breakdown

### **The Stack**
* **HTML5:** Semantic structure for accessibility and SEO.
* **CSS3 (Advanced):** * **Custom Properties:** Centralized variables for instant theming.
    * **Keyframe Animations:** Smooth, hardware-accelerated background movement.
    * **Flexbox:** Precision alignment for the glass container.
* **Vanilla JavaScript:** * Zero-dependency logic for maximum performance.
    * Dynamic DOM manipulation to update the `<iframe>` without page refreshes.

### **The Logic**
The application uses a sophisticated regex to ensure the user doesn't have to worry about "clean" links. It strips away tracking parameters like `?si=` or `&feature=shared` automatically:

```javascript
const regex = /(?:youtube\.com\/(?:[^\/]+\/.+\/|(?:v|e(?:mbed)?|shorts)\/|.*[?&]v=)|youtu\.be\/)([^"&?\/\s]{11})/;
.
├── index.html        # The entire application (HTML/CSS/JS)
└── README.md         # Project documentation
Developed with ❤️ by DIPTARAFDER

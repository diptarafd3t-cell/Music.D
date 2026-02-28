# Music.D
# 🎵 MUSIC-D (sub-use)

A professional, ultra-modern YouTube video player interface featuring a cinematic **Glassmorphism** design. This single-page application uses dynamic background animations and a robust URL parser to provide a premium viewing experience.

![Version](https://img.shields.io/badge/Version-1.0.0-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![UI-Style](https://img.shields.io/badge/Style-Glassmorphism-purple)

## ✨ Key Features

- **Glassmorphism UI:** Implements `backdrop-filter: blur()` and subtle white borders to create a "frosted glass" effect.
- **Animated Ambient Background:** Three distinct "blobs" (Indigo, Pink, and Red) that drift and scale automatically to create a dynamic visual atmosphere.
- **Smart URL Parser:** Uses an advanced Regular Expression (Regex) to extract Video IDs from multiple YouTube URL formats (Desktop, Mobile, Shortened, and Embeds).
- **Responsive Design:** Fully optimized for mobile, tablet, and desktop screens with a fluid 16:9 video aspect ratio.
- **Premium Typography:** Integrated with Google Fonts using the *Plus Jakarta Sans* typeface.
- **Interaction:** Supports both button clicks and "Enter" key submission for seamless navigation.

## 🚀 Quick Start

1. **Save the Code:** Create a new file named `index.html`.
2. **Paste & Save:** Paste the project code into that file.
3. **Launch:** Open `index.html` in any modern web browser.
4. **Play:** 
   - Find a YouTube link (e.g., `https://www.youtube.com/watch?v=dQw4w9WgXcQ`).
   - Paste it into the input box.
   - Click **"Load Video"** to update the cinema screen.

## 🛠️ Built With

*   **HTML5:** Semantic structure.
*   **CSS3:** 
    - Custom Properties (Variables) for theming.
    - Keyframe Animations for background movement.
    - Flexbox for layout alignment.
    - Glassmorphism effects (`-webkit-backdrop-filter`).
*   **JavaScript (Vanilla):** 
    - Regex-based URL validation.
    - DOM manipulation for dynamic source updating.

## 🧪 Technical Details

The core logic resides in the `updateVideo()` function, which cleans user input to find the unique 11-character YouTube ID:

```javascript
const regex = /(?:youtube\.com\/(?:[^\/]+\/.+\/|(?:v|e(?:mbed)?)\/|.*[?&]v=)|youtu\.be\/)([^"&?\/\s]{11})/;

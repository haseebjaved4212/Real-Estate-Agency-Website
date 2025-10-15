# Real Estate Digital Twin Token platform


A single-page scrolling experience inspired by Magma, built with HTML, CSS, and JavaScript. It uses GSAP ScrollTrigger, Locomotive Scroll, canvas-driven frame sequences, and simple text animations to create a smooth, immersive landing page.

## Overview

- Smooth scrolling and scroll-driven animations
- Pinned canvas sections rendering frame-by-frame image sequences
- Text reveal animations via span-wrapped characters
- Responsive layout across screen sizes
- Uses CDN libraries (GSAP, ScrollTrigger, Locomotive Scroll, Remix Icon)

## Demo
[Real Estate Agency Website]( https://haseebjaved4212.github.io/Real-Estate-Agency-Website/)

## Tech Stack

- HTML5
- CSS3
- JavaScript (ES6)
- GSAP 3 + ScrollTrigger (via CDN)
- Locomotive Scroll (via CDN)
- Remix Icon (via CDN)

## File Structure

```text
├── index.html
├── style.css
├── script.js
└── Assets/
├── Images/
│ └── Screenshot 2023-05-30 220719.png (Logo used in nav)
├── Fonts/
│ ├── jost-variable.ttf (font-family: a)
│ ├── KFOlCnqEu92Fr1MmEU9fBBc4 (1).ttf (font-family: b)
│ └── KFOmCnqEu92Fr1Mu4mxK (1).ttf (font-family: c)
├── Frames/ (Page 3 canvas sequence)
│ ├── frames00007.png
│ ├── frames00010.png
│ ├── ...
│ └── frames00202.png
└── Bridges/ (Page 5 canvas sequence)
├── bridges00004.png
├── bridges00007.png
├── ...
└── bridges00202.png
```


**⚠️ Note:** If you keep assets at the project root, update the paths in `HTML/CSS/JS` accordingly. Web paths should use forward slashes (/) even on Windows.

## Assets and Paths

- Images
  - Nav logo in `index.html` references `./Assets/Images/Screenshot 2023-05-30 220719.png` (recommended).
  - If you keep it at project root, update the src accordingly (e.g., `./Screenshot 2023-05-30 220719.png`).

- Fonts (style.css)
  - jost-variable.ttf → `./Assets/Fonts/jost-variable.ttf`
  - KFOlCnqEu92Fr1MmEU9fBBc4 (1).ttf → `./Assets/Fonts/KFOlCnqEu92Fr1MmEU9fBBc4 (1).ttf`
  - KFOmCnqEu92Fr1Mu4mxK (1).ttf → `./Assets/Fonts/KFOmCnqEu92Fr1Mu4mxK (1).ttf`
  - If file names include spaces/parentheses, keep them as-is or rename and update CSS.

- Frames (script.js, Page 3)
  - Place all `framesNNNNN.png` files in `Assets/Frames/`.
  - Ensure the list in `files(index)` points to `./Assets/Frames/framesXXXXX.png` consistently.

- Bridges (script.js, Page 5)
  - Place all `bridgesNNNNN.png` files in `Assets/Bridges/`.
  - Ensure the list in `files(index)` points to `./Assets/Bridges/bridgesXXXXX.png`.

- Remote sequences (Page 7)
  - These are loaded from `https://thisismagma.com/assets/home/lore/seq/*.webp`. Internet connectivity is required.

- Videos and External Media
  - Page 1 Hero video: `https://thisismagma.com/wp-content/themes/magma/assets/home/hero/1.mp4?2`
  - Page 8 Glass video: `https://thisismagma.com/wp-content/themes/magma/assets/home/glass/1.webm?2`
  - Blog images and background image in CSS load from `thisismagma.com` CDNs.

## Getting Started

- Prerequisites
  - A modern browser
  - Internet access for CDNs and remote assets
  - Optional: a local static server for best behavior (e.g., VSCode Live Server or any simple HTTP server)

- Run Locally
  1. Place the project folder anywhere on your machine.
  2. Put images, fonts, and frame sequences into the `Assets/` subfolders as described.
  3. Open `index.html`directly in your browser, or serve the folder with a local server.

## ✨ Features

- Smooth scrolling provided by Locomotive Scroll with GSAP ScrollTrigger scrollerProxy integration
- Pinned canvas sections that render large image sequences efficiently
- Text animation using span-wrapped characters for color progression
- Responsive layout with media queries for different viewport sizes

## How It Works

- Smooth Scrolling
  - Locomotive Scroll is initialized on `#main`.
  - ScrollTrigger uses `scrollerProxy` to sync GSAP with Locomotive’s scroll container.

- Text Animation
  - Headings on pages 2, 4, and 6 are split into spans and animated with ScrollTrigger to change color during scroll.

- Canvas Sequences
  - Pages 3 and 5 use `<canvas>` to render image sequences (`Frames` and `Bridges` respectively).
  - Images are preloaded into arrays; ScrollTrigger updates a frame index and render draws the current image, scaled to fit.

- Pinned Sections
  - ScrollTrigger pins the canvas sections while the frame animation plays (e.g., `end: "250% top"`).

## Customization

- Change copy in `index.html`
- Update styling in `style.css` (colors, sizes, spacing).
- Swap fonts by replacing files in `Assets/Fonts/` and updating @font-face entries.
- Replace image sequences by dropping new files in `Assets/Frames/` or `Assets/Bridges/` and updating the lists in `script.js`
## Troubleshooting

- Broken paths
  - Ensure your assets exist in the paths referenced by HTML/CSS/JS.
  - Use forward slashes (/) in paths.
  - If filenames contain spaces or parentheses, keep them consistent with the references.

- CDN issues
  - If CDNs are blocked or offline, download libraries locally and link them from your project.

- Performance
  - Large image sequences can be heavy. Optimize PNGs or convert to WebP when possible.

## Browser Support

- Modern browsers (Chrome, Edge, Firefox, Safari)
- Mobile browsers supported via responsive CSS and standard web APIs

## License

This project is provided as-is for educational and demonstration purposes. Please ensure you have rights to any media assets used.

---
<div align="center"> 
Made with ❤️ by Haseeb Javed </div>

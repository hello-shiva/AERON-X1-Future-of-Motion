# AERON X1 — Additional Info for Judges

## How to run the project
This is a single self-contained HTML file — no build step, no install, no server required.

1. Open `source/index.html` in a modern desktop browser (Chrome, Edge, or Firefox recommended — WebGL2 required).
2. Scroll to move through the cinematic experience.
3. Try the interactive features:
   - **Inspect Machine** (bottom-right button) — click parts of the bike for specs
   - **Build Your Aeron** (Configure section) — change body finish, wheel finish, and lighting live
   - **Enter the Machine** — full-screen cockpit HUD mode
   - Sound toggle (top-right) for ambient audio
   - Easter eggs: click the "AERON" logo 5 times, or try the Konami code (↑↑↓↓←→←→ B A)

No external assets are loaded except the Three.js library and Google Fonts, both from public CDNs — everything else (the motorcycle geometry, materials, lighting, camera choreography) is generated in-browser by the code in this one file.

## What's in this zip
- `source/index.html` — the full project source (Three.js scene, UI, and logic in one file)
- `media/aeron-thumbnail.png` — project thumbnail (3:2)
- `media/aeron-gallery-*.png` — gallery images used on the project page, one per major section (Hero, Design, Performance, Configure, Cockpit)
- `media/aeron-x1-teaser.mp4` — a short motion-graphics teaser assembled from the gallery frames (uploaded separately to YouTube for the video demo link)

## Tech stack
Three.js, vanilla JavaScript (ES modules), HTML5, CSS3, WebGL, GLSL (post-processing), Web Audio API. No build tooling, no framework, no external 3D asset files — the motorcycle is generated procedurally at runtime.

## Notes on the build process
The 3D motorcycle is built entirely from primitive and extruded geometry rather than an imported model, so every surface, wheel, and light is composed and lit in code. A PMREM-generated environment map gives the metal/carbon materials realistic reflections, and an UnrealBloomPass post-processing pass handles the glow on lights and accent lines. Camera movement through the scroll-driven scenes is hand-interpolated between keyframes rather than using a scroll-animation library, keeping the whole thing dependency-light.

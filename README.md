# AERON X1 — Future of Motion

An immersive, scroll-driven 3D website for a fictional electric superbike, built entirely with **Three.js**. No build step, no external 3D assets, no frameworks — the motorcycle, its materials, lighting, and camera choreography are all generated in a single HTML file.

![AERON X1 thumbnail](media/aeron-thumbnail.png)

## ✨ Features

- **Cinematic scroll-driven camera** — scrolling moves the camera through a sequence of directed shots (Reveal → Design → Power → Aerodynamics → Intelligence → Performance), not just a spinning model
- **Procedurally built motorcycle** — the entire bike (frame, fairing, wheels, suspension, motor, exhaust) is generated from code, no imported 3D model
- **Assembly-from-light intro** — the bike fades in from a glowing wireframe blueprint into a fully solid model on first scroll
- **Inspect Machine mode** — click any part of the bike to pull up specs on the battery, motor, frame, suspension, and wheels
- **Live configurator** — change body finish, wheel finish, and lighting mode and watch the actual 3D materials update in real time
- **Enter the Machine** — a full-screen cockpit mode with an animated HUD (speed, RPM, battery, riding mode)
- **Realistic lighting** — PMREM-generated environment map + bloom post-processing so metal and carbon surfaces pick up real reflections
- **Ambient audio** — a low engine-like hum generated with the Web Audio API (no external sound files)
- **Easter eggs** — click the logo 5 times, try the Konami code, or double-click the headlight

## 🖼️ Preview

| Design | Performance |
|---|---|
| ![Design](media/aeron-gallery-02-design.png) | ![Performance](media/aeron-gallery-03-performance.png) |

| Configurator | Cockpit |
|---|---|
| ![Configurator](media/aeron-gallery-04-configurator.png) | ![Cockpit](media/aeron-gallery-05-cockpit.png) |

## 🚀 Getting started

No installation or build step required.

```bash
git clone https://github.com/your-username/aeron-x1.git
cd aeron-x1
```

Then just open `source/index.html` in a modern desktop browser (Chrome, Edge, or Firefox — WebGL2 required).

Or serve it locally if you'd rather not open the file directly:

```bash
npx serve source
```

## 🕹️ How to use it

- **Scroll** to move through the cinematic experience
- **Move your mouse** on the hero screen for parallax
- **Inspect Machine** (bottom-right button) → click a part of the bike for its spec panel
- **Build Your Aeron** (Configure section) → pick a body finish, wheel finish, and lighting mode
- **Enter the Machine** → full cockpit HUD; **Exit Machine** to leave
- **Sound toggle** (top-right) → ambient engine hum

## 🛠️ Tech stack

- [Three.js](https://threejs.org/) — scene, geometry, materials, lighting
- `EffectComposer` + `UnrealBloomPass` — post-processing / glow
- `PMREMGenerator` + `RoomEnvironment` — realistic reflections on metal/carbon
- Vanilla JavaScript (ES modules) — scroll choreography, UI, configurator logic
- Web Audio API — ambient sound, no external audio files
- HTML5 / CSS3 — layout, typography, HUD UI

No React, no bundler, no npm install — everything loads from CDN via an import map.

## 📁 Project structure

```
aeron-x1/
├── source/
│   └── index.html       # entire app: scene, UI, and logic in one file
├── media/                # thumbnail, gallery images, teaser video
└── README.md
```

## 📌 Notes

This is a concept/demo project built for a hackathon-style showcase. The motorcycle is fictional, and the "specs" shown (top speed, range, etc.) are illustrative, not real-world figures.

##  🖊️ ** Author**
- Shivam Kumar(BTech CSE Student)
## 📄 License
MIT — feel free to fork, remix, and build on it.

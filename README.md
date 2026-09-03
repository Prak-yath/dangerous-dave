# 🕹️ Dangerous Dave — 2026 Redux

<p align="center">
  <img src="https://img.shields.io/badge/status-active-brightgreen" alt="status">
  <img src="https://img.shields.io/badge/built%20with-HTML5%20%7C%20CSS3%20%7C%20JavaScript-yellow" alt="tech">
  <img src="https://img.shields.io/badge/dependencies-none-blue" alt="dependencies">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey" alt="license">
  <img src="https://img.shields.io/badge/platform-web-orange" alt="platform">
</p>

<p align="center">
  An enhanced, from-scratch reimagining of the 1988 platformer classic <b>Dangerous Dave</b> — rebuilt with modern movement physics, accessibility features, mobile support, and significantly improved game feel.
</p>

<p align="center">
  <b><a href="https://prak-yath.github.io/dangerous-dave/">▶ Play the Live Demo</a></b>
</p>

---

## 📑 Table of Contents

- [About the Project](#-about-the-project)
- [Problem Statement](#-problem-statement)
- [Objectives](#-objectives)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Controls](#-controls)
- [How It Works](#-how-it-works)
- [Original vs. Redux Comparison](#-original-vs-redux-comparison)
- [Screenshots](#-screenshots)
- [Future Scope](#-future-scope)
- [Team](#-team)
- [Acknowledgements](#-acknowledgements)
- [License](#-license)

---

## 📖 About the Project

**Dangerous Dave — 2026 Redux** is a browser-based, side-scrolling cave-exploration platformer inspired by the 1988 DOS classic *Dangerous Dave* by John Romero. Rather than emulating the original's assets, this project is a **complete ground-up rebuild** — every sprite, sound, level, and physics system is written from scratch using only native web technologies.

The goal was twofold:
1. Recreate the core experience that made the original memorable — cave exploration, trophy collecting, a jetpack sequence, and a simple gun mechanic.
2. Systematically identify and fix the usability, accessibility, and design shortcomings that a 2026 audience would find frustrating in a nearly 40-year-old game.

The result is a fully playable, responsive, offline-capable game delivered as a **single HTML file** with zero external dependencies.

---

## ❓ Problem Statement

Classic 1980s/90s platformers, while historically significant, exhibit several design and technical limitations by modern standards:

- Movement feels stiff, with no acceleration or deceleration curves
- Hitboxes are pixel-perfect and unforgiving, leading to "unfair" deaths
- A single hit often forces a full level restart, with no checkpoint system
- Controls are hardcoded to arrow keys only, with no remapping and no mobile support
- There is no pause menu, difficulty setting, volume control, or accessibility options
- Progress is never saved between sessions
- Mandatory collectible requirements (e.g., "collect all trophies to open the door") can trap players and force tedious backtracking

This project addresses each of these issues directly, using the original game as a case study in platformer UX design evolution.

---

## 🎯 Objectives

- Rebuild a classic platformer's core mechanics using only HTML5 Canvas and vanilla JavaScript (no game engine)
- Apply modern game-feel principles: acceleration-based movement, coyote-time, jump-buffering, and forgiving collision detection
- Design an accessible experience: difficulty modes, high-contrast mode, reduced-motion support, and full keyboard + touch input
- Implement a save/progress system using browser storage
- Document every design decision as a direct comparison against the shortcomings of the original

---

## ✨ Features

### Core Gameplay
- Physics-driven platforming with acceleration/friction, coyote-time, and jump-buffering
- Optional trophies that add score and build a combo multiplier — never mandatory to progress
- Rechargeable jetpack for free-flight sections
- Pickup-able gun for shooting enemies
- Lives system with mid-level checkpoint flags and post-hit invulnerability frames
- Patrolling and flying enemies with readable, learnable movement patterns
- Forgiving hazard hitboxes (spikes, lava) shrunk from the visible sprite
- A visibly sign-posted warp shortcut on one level

### Levels & Progression
- 4 hand-built levels, each with a distinct palette and pacing
- Level-select screen showing lock state, best time, and medal earned
- Bronze / Silver / Gold medal system based on completion time vs. a par time
- Persistent progress: level unlocks, best times, and high scores saved locally

### Accessibility & Difficulty
- Easy / Normal / Hardcore difficulty modes
- High-contrast player sprite option
- Reduce-motion toggle for particle effects
- Independent screen-shake toggle
- Independent music and SFX volume sliders with instant mute

### Controls & Platform Support
- Full WASD **and** Arrow-key support simultaneously
- On-screen touch controls that auto-appear on mobile devices
- Fully responsive canvas — scales cleanly from phone to desktop

### Presentation
- Neon cave color palette with parallax depth layers
- Screen shake, hit-flash, and particle effects for game feel
- Optional retro CRT scanline filter
- All audio procedurally synthesized live via the Web Audio API — zero audio files

---

## 🛠 Tech Stack

| Layer | Technology |
| --- | --- |
| Rendering | HTML5 `<canvas>` (2D context) |
| Logic | Vanilla JavaScript (ES6+) |
| Styling | CSS3 |
| Audio | Web Audio API (procedural synthesis) |
| Persistence | Browser `localStorage` |
| Build tooling | None — no bundler, framework, or external library required |

This project deliberately avoids frameworks and game engines to demonstrate that a complete, polished game loop — physics, rendering, audio, state management, and UI — can be built with core web platform APIs alone.

---

## 📂 Project Structure

```
dangerous-dave/
│
├── index.html          # Entire game: markup, styles, and game logic in one file
└── README.md            # Project documentation
```

The game is intentionally kept as a single self-contained file so it can be run, shared, or hosted with zero setup.

---

## 🚀 Getting Started

### Prerequisites

- Any modern web browser (Chrome, Edge, Firefox, Safari)
- No installation, package manager, or build tools required

### Installation

1. Download or clone this repository.
2. Open `index.html` directly in your browser — that's the entire setup.

Optionally, for live-reload while editing, open the folder in VS Code and use the **Live Server** extension.

---

## 🎮 Controls

| Input | Action |
| --- | --- |
| `W` `A` `S` `D` or Arrow Keys | Move left/right, jump, duck |
| `Space` / `W` / `↑` | Jump — hold to fly once the jetpack is found |
| `F` / `J` | Fire gun (once picked up) |
| `P` / `Esc` | Pause |
| `R` | Restart from the last checkpoint |
| On-screen D-pad / buttons | Full touch equivalent, auto-shown on mobile |

---

## ⚙️ How It Works

- **Game loop:** driven by `requestAnimationFrame`, with delta-time-based physics so movement speed stays consistent across different frame rates.
- **Physics:** the player has horizontal acceleration and friction rather than instant velocity changes; jump timing uses coyote-time (a short grace window after leaving a platform) and jump-buffering (registering a jump input slightly before landing).
- **Collision detection:** axis-aligned bounding box (AABB) checks against level geometry, with hitboxes intentionally inset from the visible sprite to keep near-misses feeling fair.
- **Level data:** each level is defined as a structured JavaScript object describing platform positions, hazards, enemy patrol paths, collectibles, and the exit door — making levels easy to extend or add to.
- **State & persistence:** game state (lives, score, current checkpoint) is held in memory during play; unlocked levels, best times, and high scores are written to `localStorage` so progress survives a page refresh.
- **Audio:** every sound effect and music note is generated at runtime using Web Audio API oscillators — there are no `.mp3` or `.wav` files in the project.

---

## 🔄 Original vs. Redux Comparison

| 1988 Original | 2026 Redux |
| --- | --- |
| Arrow keys only | WASD + Arrows + full touch controls |
| Stiff, floaty movement | Acceleration/friction physics, coyote-time, jump-buffering |
| One hit resets the whole level | Lives, mid-level checkpoints, brief invulnerability |
| All trophies mandatory to open the door | Trophies are optional bonus score — the door is always open |
| No pause, no settings, no volume control | Full pause menu, music/SFX sliders, mute |
| Fixed low resolution, desktop-only | Responsive canvas, phone to desktop, touch-ready |
| No progress saving | Level unlocks, best times, and high scores saved locally |
| Flat EGA color blocks | Neon palette, parallax, particles, optional CRT filter |

---

## 🖼 Screenshots

> _Add gameplay screenshots or a short GIF here once available, e.g.:_
> `![Gameplay](./screenshots/gameplay.png)`

---

## 🔮 Future Scope

- [ ] Dedicated CGA/EGA retro color-palette mode
- [ ] Native gamepad support
- [ ] Boss encounter for the final level
- [ ] In-browser level editor for building and sharing custom levels
- [ ] Online leaderboard for best times

---

## 👥 Team

| USN | Name |
| --- | --- |
| NNM23IS129 | Prakyath P Nayak |
| NNM23IS131 | Pranav P Nayak |

---

## 🙏 Acknowledgements

- Inspired by *Dangerous Dave* (1988), created by John Romero and Id Software's founding team, published by Softdisk.
- Built as an educational exercise in game-loop architecture, platformer physics, and web-native audio/visual synthesis.

---

## 📄 License

No license has been added yet. If this project is intended to be shared or reused publicly, consider adding an [MIT License](https://choosealicense.com/licenses/mit/) or similar.

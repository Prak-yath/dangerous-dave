# 🕹️ Dangerous Dave — 2026 Redux


<p align="center">
  A from-scratch modern reimagining of the 1988 platformer classic, rebuilt with modern physics, responsive controls, accessibility features, and a retro-neon visual style.
</p>

<p align="center">
  <b><a href="https://prak-yath.github.io/dangerous-dave/">▶ Play the Live Demo</a></b>
</p>

---

## 📑 Table of Contents

- [About the Game](#-about-the-game)
- [Screenshots](#-screenshots)
- [Features](#-features)
- [Levels & Progression](#️-levels--progression)
- [Controls](#-controls)
- [Accessibility & Difficulty](#-accessibility--difficulty)
- [Visual & Audio Design](#-visual--audio-design)
- [Progress Saving](#-progress-saving)
- [Responsive & Offline](#-responsive--offline)
- [Technical Stack](#️-technical-stack)
- [Original vs. 2026 Redux](#-original-vs-2026-redux)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Current Status](#-current-status)
- [Future Improvements](#-future-improvements)
- [Inspiration](#-inspiration)
- [Team](#-team)
- [License](#-license)

---

## 🎮 About the Game

**Dangerous Dave — 2026 Redux** is a from-scratch reimagining of the classic 1988 platformer.

The project keeps the core idea of cave exploration and platforming while introducing modern game-feel improvements such as acceleration-based movement, coyote time, jump buffering, checkpoints, optional collectibles, power-ups, responsive controls, and local progress saving.

The game runs completely in the browser and requires no installation, account, internet connection, or external game engine.

---

## ✨ Features

### 🏃 Core Gameplay

| Category | Details |
| --- | --- |
| Movement | Acceleration and friction-based physics-driven platforming |
| Jump feel | Coyote time and jump buffering |
| Collectibles | Optional trophy collectibles with a combo multiplier and completion bonus |
| Power-ups | Rechargeable jetpack, pickup-able gun |
| Enemies | Ground and flying enemies |
| Hazards | Spikes and lava |
| Survivability | Lives, mid-level checkpoints, temporary invulnerability after damage |
| Bonus route | Sign-posted warp shortcut |

---

## 🗺️ Levels & Progression

| Level | Theme |
| --- | --- |
| 1 | Cave Entrance |
| 2 | The Lower Shaft |
| 3 | Jetpack Ascent |
| 4 | Deep Warp Zone |

Each level has its own palette, hazards, pacing, and challenges.

**Additional progression features:**

| Feature | Description |
| --- | --- |
| Level-select map | Shows lock/unlock state for each level |
| Best-time tracking | Records your fastest completion per level |
| Medals | Bronze, Silver, and Gold based on completion time |
| Run recap | Displays time, deaths, and score after each level |
| Progress saving | Local save data, persists between sessions |
| High scores | Saved persistently |

---

## 🎯 Controls

| Input | Action |
| --- | --- |
| `W` `A` `S` `D` | Move, jump, duck |
| Arrow Keys | Move and jump |
| `Space` | Jump / jetpack flight |
| `F` / `J` | Fire gun |
| `P` / `Esc` | Pause |
| `R` | Restart from checkpoint |
| Touch Controls | On-screen D-pad, jump, and fire buttons — appear automatically on mobile devices |

---

## ♿ Accessibility & Difficulty

### Accessibility Options

| Option | Description |
| --- | --- |
| High-contrast mode | High-contrast player sprite |
| Reduce motion | Reduces particle/motion effects |
| Screen shake | Independent on/off toggle |
| Music volume | Adjustable slider |
| SFX volume | Adjustable slider |
| Mute | Instant mute for all audio |

### Difficulty Modes

| Mode | Lives | Checkpoints | Enemy Speed |
| --- | --- | --- | --- |
| 🟢 Easy | 5 | Yes | Normal |
| 🟡 Normal | 3 | Yes | Normal |
| 🔴 Hardcore | 1 | No | Faster |

---

## 🎨 Visual & Audio Design

The game uses a **neon cave aesthetic** with:

| Visual Effects | Audio |
| --- | --- |
| Parallax depth layers | Procedural sound via Web Audio API |
| Glowing trophies | No external sound files required |
| Animated jetpack particle trails | Live-generated music and SFX |
| Particle effects, screen shake, hit flashes | — |
| Pickup and kill effects | — |
| Optional CRT scanline filter | — |
| Responsive canvas scaling | — |

All visuals are rendered live without image assets.

---

## 💾 Progress Saving

Game progress is stored locally using the browser's **Local Storage API**.

| Data Saved | Persists Between Sessions |
| --- | --- |
| Unlocked levels | ✅ |
| Best times | ✅ |
| High scores | ✅ |

---

## 📱 Responsive & Offline

| Platform | Supported |
| --- | --- |
| 💻 Desktop | ✅ |
| 📱 Mobile | ✅ |
| 🌐 Modern browsers | ✅ |

The game uses a fixed internal resolution of **960 × 540**, fluidly scaled to fit different screen sizes. The entire game is contained in a single HTML file and can run completely offline.

---

## 🛠️ Technical Stack

| Technology | Purpose |
| --- | --- |
| HTML5 Canvas | Game rendering |
| Vanilla JavaScript | Game logic and mechanics |
| Web Audio API | Procedural sound and music |
| Local Storage | Save data |
| CSS | Responsive display and interface |

### No External Dependencies

The project intentionally avoids:

| ❌ Excluded |
| --- |
| Game engines |
| Build systems |
| External game libraries |
| Image assets |
| Audio files |
| Internet connection requirement |

---

## 🔄 Original vs. 2026 Redux

| 1988 Original | 2026 Redux |
| --- | --- |
| Arrow keys only | WASD + Arrow keys + Touch |
| Stiff movement | Acceleration + friction physics |
| Basic jumping | Coyote time + jump buffering |
| One hit resets the level | Lives + checkpoints |
| Trophies required | Trophies are optional |
| No pause/settings | Full pause menu + settings |
| Desktop-focused | Responsive mobile + desktop |
| No progress saving | Local progress saving |
| Flat EGA visuals | Neon visuals + particles + parallax |
| Limited feedback | Screen shake + hit effects |
| No modern audio system | Procedural Web Audio |

---

## 🚀 Getting Started

### Option 1 — Run Locally

1. Clone the repository:
   ```
   git clone https://github.com/Prak-yath/dangerous-dave.git
   ```
2. Open the project folder.
3. Open the `.html` file in a modern web browser.

That's it — no installation or build process required.

### Option 2 — Play Offline

Because the game is delivered as a single HTML file, you can keep the file on your device and open it whenever you want to play — no internet connection needed.

---

## 📂 Project Structure

```
dangerous-dave/
│
├── index.html
├── screenshots/
│   ├── title-screen.png
│   └── jetpack-ascent-gameplay.png
└── README.md
```

The game is designed as a single-file HTML project, keeping deployment simple and portable.

---

## 🧪 Current Status

**Version:** 2026 Redux

| Feature | Status |
| --- | --- |
| Platforming physics | ✅ |
| Coyote time | ✅ |
| Jump buffering | ✅ |
| Trophies and scoring | ✅ |
| Jetpack | ✅ |
| Gun | ✅ |
| Enemies | ✅ |
| Hazards | ✅ |
| Lives | ✅ |
| Checkpoints | ✅ |
| Warp shortcut | ✅ |
| Four levels | ✅ |
| Level selection | ✅ |
| Medals | ✅ |
| Progress saving | ✅ |
| Touch controls | ✅ |
| Accessibility options | ✅ |
| Difficulty modes | ✅ |
| Procedural audio | ✅ |
| CRT filter | ✅ |
| Responsive display | ✅ |

---

## 🔮 Future Improvements

| Planned Feature | Description |
| --- | --- |
| 🎨 Retro palette mode | Dedicated CGA/EGA color-swap mode |
| 🎮 Gamepad support | Native gamepad input alongside keyboard/touch |
| 👹 Boss fight | Final-level boss encounter |
| 🧱 Level editor | In-browser level editor |
| 🌐 Custom level sharing | Share user-built levels |

---

## 📜 Inspiration

This project is inspired by the original *Dangerous Dave*, while being rebuilt from scratch with a modern approach to gameplay, controls, accessibility, presentation, and browser technology.

The goal is not simply to reproduce the original game, but to explore how a classic platformer could feel if redesigned for modern players.

---

## 👥 Team

| USN | Name |
| --- | --- |
| NNM23IS129 | Prakyath P Nayak |
| NNM23IS131 | Pranav P Nayak |

---

## 📄 License

No license has been added yet. If this project is intended to be shared or reused publicly, consider adding an [MIT License](https://choosealicense.com/licenses/mit/) or similar.

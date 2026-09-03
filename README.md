🕹️ Dangerous Dave — 2026 Redux
A from-scratch modern reimagining of the 1988 platformer classic, rebuilt with modern physics, responsive controls, accessibility features, and a retro-neon visual style.

🎮 About the Game
Dangerous Dave — 2026 Redux is a from-scratch reimagining of the classic 1988 platformer.

The project keeps the core idea of cave exploration and platforming while introducing modern game-feel improvements such as acceleration-based movement, coyote time, jump buffering, checkpoints, optional collectibles, power-ups, responsive controls, and local progress saving.

The game runs completely in the browser and requires no installation, account, internet connection, or external game engine.

✨ Features
🏃 Core Gameplay
Physics-driven platforming
Acceleration and friction-based movement
Coyote time and jump buffering
Optional trophy collectibles
Trophy combo multiplier and completion bonus
Rechargeable jetpack
Pickup-able gun
Ground and flying enemies
Spikes and lava hazards
Lives and mid-level checkpoints
Temporary invulnerability after taking damage
Sign-posted warp shortcut
🗺️ Levels & Progression
The game contains 4 hand-built levels:

Cave Entrance
The Lower Shaft
Jetpack Ascent
Deep Warp Zone
Each level has its own palette, hazards, pacing, and challenges.

Additional progression features include:

Level-select map
Level lock/unlock states
Best-time tracking
Bronze, Silver, and Gold medals
Run recap showing time, deaths, and score
Local progress saving
Persistent high scores
🎯 Controls
Input

Action

W / A / S / D

Move, jump, duck

Arrow Keys

Move and jump

Space

Jump / Jetpack flight

F / J

Fire gun

P / Esc

Pause

R

Restart from checkpoint

Touch Controls

D-pad, jump and fire buttons

Touch controls automatically appear on mobile devices.

♿ Accessibility & Difficulty
Accessibility
High-contrast player sprite
Reduce-motion option
Independent screen-shake toggle
Music volume control
SFX volume control
Instant mute
Difficulty Modes
Mode

Lives

Checkpoints

Enemy Speed

🟢 Easy

5

Yes

Normal

🟡 Normal

3

Yes

Normal

🔴 Hardcore

1

No

Faster

🎨 Visual & Audio Design
The game uses a neon cave aesthetic with:

Parallax depth layers
Glowing trophies
Animated jetpack particle trails
Particle effects
Screen shake
Hit flashes
Pickup and kill effects
Optional CRT scanline filter
Responsive canvas scaling
All visuals are rendered live without image assets.

Audio is also generated live in the browser using the Web Audio API, meaning the game does not require external sound files.

💾 Progress Saving
Game progress is stored locally using the browser’s Local Storage API.

The following information can persist between sessions:

Unlocked levels
Best times
High scores
📱 Responsive & Offline
The game is designed to work across:

💻 Desktop
📱 Mobile
🌐 Modern browsers
It uses a fixed internal resolution of 960 × 540, which is fluidly scaled to fit different screen sizes.

The entire game is contained in a single HTML file and can run completely offline.

🛠️ Technical Stack
Technology

Purpose

HTML5 Canvas

Game rendering

Vanilla JavaScript

Game logic and mechanics

Web Audio API

Procedural sound and music

Local Storage

Save data

CSS

Responsive display and interface

No External Dependencies
The project intentionally avoids:

❌ Game engines
❌ Build systems
❌ External game libraries
❌ Image assets
❌ Audio files
❌ Internet connection
🔄 Original vs. 2026 Redux
1988 Original

2026 Redux

Arrow keys only

WASD + Arrow keys + Touch

Stiff movement

Acceleration + friction physics

Basic jumping

Coyote time + jump buffering

One hit resets the level

Lives + checkpoints

Trophies required

Trophies are optional

No pause/settings

Full pause menu + settings

Desktop-focused

Responsive mobile + desktop

No progress saving

Local progress saving

Flat EGA visuals

Neon visuals + particles + parallax

Limited feedback

Screen shake + hit effects

No modern audio system

Procedural Web Audio

🚀 Getting Started
Option 1 — Run Locally
Clone the repository:
git clone https://github.com/YOUR-USERNAME/dangerous-dave-2026-redux.git
Open the project folder.
Open the .html file in a modern web browser.
That’s it.

No installation or build process is required.

Option 2 — Play Offline
Because the game is delivered as a single HTML file, you can simply keep the file on your device and open it whenever you want to play.

📂 Project Structure
dangerous-dave-2026-redux/
│
├── index.html
└── README.md
The game is designed as a single-file HTML project, keeping deployment simple and portable.

🧪 Current Status
Version: 2026 Redux

Implemented
☑ Platforming physics
☑ Coyote time
☑ Jump buffering
☑ Trophies and scoring
☑ Jetpack
☑ Gun
☑ Enemies
☑ Hazards
☑ Lives
☑ Checkpoints
☑ Warp shortcut
☑ Four levels
☑ Level selection
☑ Medals
☑ Progress saving
☑ Touch controls
☑ Accessibility options
☑ Difficulty modes
☑ Procedural audio
☑ CRT filter
☑ Responsive display
🔮 Future Improvements
Possible future additions include:

🎨 Dedicated CGA/EGA retro palette mode
🎮 Gamepad support
👹 Final-level boss fight
🧱 In-browser level editor
🌐 Custom level sharing
📜 Inspiration
This project is inspired by the original Dangerous Dave, while being rebuilt from scratch with a modern approach to gameplay, controls, accessibility, presentation, and browser technology.

The goal is not simply to reproduce the original game, but to explore how a classic platformer could feel if redesigned for modern players.

📄 License
Add your chosen license here, for example:

MIT License
If this project uses original copyrighted assets, code, music, or other material from the original game, make sure the repository’s licensing and distribution terms are appropriate.

👨‍💻 Author
Prakyath Nayak

Built as a browser-based game development project using vanilla HTML5, CSS, and JavaScript.

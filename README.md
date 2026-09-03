# Dangerous Dave — 2026 Redux

An enhanced, from-scratch reimagining of the 1988 platformer classic — modern physics, accessibility options, and mobile support. Single self-contained HTML file, zero installs.

**▶ Play it live:** https://prak-yath.github.io/dangerous-dave/

## Team

| USN | Name |
| --- | --- |
| NNM23IS129 | Prakyath P Nayak |
| NNM23IS131 | Pranav P Nayak |

## About

A neon-cave platformer inspired by the 1988 original, rebuilt entirely in vanilla HTML5 canvas and JavaScript — no engine, no build step. Fixes the pitfalls of the original: stiff controls, unforgiving hitboxes, no pause, no saves, and mandatory collectibles that gated progress.

## Features

- Physics-driven movement with coyote-time and jump-buffering
- Optional trophies (bonus score, never mandatory) — the door is always open
- Jetpack and gun power-ups
- Lives, checkpoints, and 3 difficulty modes (Easy/Normal/Hardcore)
- 4 hand-built levels with medals, level select, and saved progress
- Full accessibility support (high-contrast, reduce-motion, screen-shake toggle)
- WASD + Arrows + full touch controls
- Procedural audio, no image or sound assets
- Optional retro CRT filter

## Controls

| Input | Action |
| --- | --- |
| `WASD` / Arrow Keys | Move, jump, duck |
| `Space` | Jump — hold to fly with jetpack |
| `F` / `J` | Fire gun |
| `P` / `Esc` | Pause |
| `R` | Restart from checkpoint |

## Tech Stack

Vanilla HTML5 canvas + JavaScript, Web Audio API for sound, `localStorage` for saves. No frameworks, no dependencies.

## Roadmap

- [ ] CGA/EGA retro palette mode
- [ ] Gamepad support
- [ ] Boss fight
- [ ] Level editor

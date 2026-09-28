# Catch the Falling Treats! 🧺🍓

A polished browser-based arcade game built from scratch with **HTML5, CSS3, Vanilla JavaScript, and the HTML5 Canvas API**.

## Description

Control a cute woven picnic basket in a bright outdoor meadow and catch falling treats before they bounce away.

Different objects have different point values:

- 🍓 Berry = +1
- ⭐ Sunny Star = +2
- 🍪 Cookie = +3

You start with three lives. Missing an object costs one life. The game gets progressively harder as your score increases.

## Features

- Responsive HTML5 Canvas gameplay
- Smooth keyboard controls
- Arrow Keys and A / D movement
- Optional touch controls on small screens
- Three collectible treat types: berries, sunny stars, and cookies
- Score system
- Persistent high score with `localStorage`
- Three-life system
- Four difficulty levels: Easy, Medium, Hard, Extreme
- Progressive falling speed and spawn frequency
- Countdown before each run
- Pause / resume system
- P key pause shortcut
- M key mute shortcut
- Web Audio API generated sound effects
- Mute / unmute control
- Particle effects
- Score popups
- Screen shake on missed objects
- High-score celebration
- Level-up feedback
- Responsive interface
- Accessible buttons and visible keyboard focus states
- No external game engine
- No required image or audio assets
- Safe fallbacks when audio or localStorage is unavailable

## Technologies

- HTML5
- CSS3
- JavaScript (ES6+)
- HTML5 Canvas API
- Web Audio API
- LocalStorage

## Controls

| Control | Action |
|---|---|
| `←` / `→` | Move |
| `A` / `D` | Move |
| `P` | Pause / Resume |
| `M` | Mute / Unmute |
| `Space` | Start from menu |
| `Enter` | Play again after game over |

On small screens, use the on-screen LEFT and RIGHT buttons.

## How to Run

No build system or package installation is required.

### Option 1: Open directly

Open `index.html` in a modern browser.

### Option 2: VS Code Live Server

1. Open the project folder in VS Code.
2. Install/use the **Live Server** extension if desired.
3. Right-click `index.html`.
4. Choose **Open with Live Server**.

Using a local server is useful when developing and testing browser features.

## Gameplay

1. Press **START GAME**.
2. A `3 → 2 → 1 → GO!` countdown begins.
3. Move the basket horizontally.
4. Catch berries, sunny stars, and cookies.
5. Avoid letting objects fall past the bottom.
6. Every missed object removes one life.
7. Reach higher scores to unlock harder difficulty levels.
8. The game ends when all three lives are lost.
9. Your highest score is saved in the browser.

## Difficulty

| Level | Score | Difficulty |
|---|---:|---|
| 1 | 0+ | Easy |
| 2 | 10+ | Medium |
| 3 | 25+ | Hard |
| 4 | 45+ | Extreme |

Difficulty changes falling speed, spawn frequency, and the maximum number of active objects.

## Project Structure

```text
catch-the-falling-objects/
│
├── index.html
├── style.css
├── game.js
├── README.md
│
```

### `index.html`

Contains the game interface, HUD, overlays, buttons, controls, and Canvas element.

### `style.css`

Contains the sunny picnic arcade visual design, responsive layout, animations, buttons, cards, overlays, and mobile controls.

### `game.js`

Contains the complete game engine:

- Initialization
- Input handling
- Player movement
- Object spawning
- Object updates
- Collision detection
- Score management
- Lives
- Difficulty scaling
- Game states
- Countdown
- Pause/resume
- Rendering
- Particle effects
- Audio
- LocalStorage
- Restart/reset logic

## Main JavaScript Concepts

### Game loop

The game uses `requestAnimationFrame()` to repeatedly run:

```text
INPUT
  ↓
UPDATE
  ↓
COLLISION DETECTION
  ↓
GAME STATE
  ↓
RENDER
  ↓
REPEAT
```

Delta time is used so movement is reasonably consistent across different frame rates.

### Collision detection

The falling object is treated as a small collision region and compared against the basket's rectangular catch area.

### Object spawning

Objects are created at randomized horizontal positions near the top of the Canvas and move downward at configurable speeds.

### Difficulty scaling

The game selects a difficulty configuration based on the current score. Higher levels increase speed, reduce spawn intervals, and allow more simultaneous objects.

### Game states

The project uses explicit states:

```text
MENU
COUNTDOWN
PLAYING
PAUSED
GAME_OVER
```

This keeps state-specific behavior easy to understand.

### LocalStorage

The high score is saved under:

```text
catchFallingObjectsHighScore
```

The game safely falls back to a zero high score if browser storage is unavailable.

### Web Audio API

The game generates simple sound effects in JavaScript, so it does not depend on external audio files.

## Future Improvements

Possible future additions:

- Power-ups
- Boss objects
- Multiple themed levels
- Player customization
- Online leaderboard
- More mobile controls
- Additional collectible types
- Achievements
- Difficulty selection
- Settings panel
- Background music
- Cloud score synchronization

## Portfolio Notes

This project demonstrates practical frontend and game-development concepts without relying on a framework:

- Canvas rendering
- Animation loops
- Real-time input
- Collision detection
- State management
- Procedural graphics
- Responsive UI
- Browser storage
- Web Audio
- Performance-conscious rendering
- Modular JavaScript functions

## License

This project is intended as a learning and portfolio project.


## Visual Theme
This version uses a bright sunny picnic world instead of a dark futuristic UI. The playable basket is a procedural woven picnic basket, and the collectibles are berries, sunny stars, and cookies. Clouds, grass, flowers, butterflies, and pastel colors keep the game playful and readable.

# 🎮 Neon Geometry Dash Clone

A lightweight **Geometry Dash-inspired browser game** built using **HTML5 Canvas, CSS, and vanilla JavaScript**.

The project implements a simple endless-runner style game with jumping physics, obstacles, moving platforms, multiple player modes, particles, scoring, and a neon visual style — all without using an external game engine.

## ✨ Features

* 🟦 Cube-style player movement
* 🚀 Rocket gameplay mode
* ⚡ Gravity and jumping physics
* 🔺 Randomly generated obstacles
* 🟪 Moving platforms
* 🌀 Mode-changing portals
* 💥 Particle effects
* 🌌 Scrolling background
* 🏆 Score and persistent high-score system
* ⏸️ Pause functionality
* 🔄 Game-over and restart system
* 🖱️ Keyboard and mouse controls
* 🎨 Neon-inspired visual effects

## 🛠️ Built With

* **HTML5**
* **CSS3**
* **JavaScript**
* **HTML5 Canvas API**
* **Web Storage / localStorage**

No external game engine or JavaScript framework is required.

## 📂 Project Structure

```text
geometry-dash-clone/
│
├── index.html
├── player.png
├── rocket_player.png
├── bg.jpg
└── README.md
```

### Assets

* `player.png` — Cube player sprite
* `rocket_player.png` — Rocket mode sprite
* `bg.jpg` — Scrolling game background
* `index.html` — Game rendering, physics, controls and gameplay logic

## 🎮 Controls

| Control                       | Action                |
| ----------------------------- | --------------------- |
| `Space`                       | Jump / control rocket |
| `Mouse Click`                 | Jump / control rocket |
| `P`                           | Pause / resume        |
| `Space` or Click after losing | Restart game          |

## 🧠 How It Works

The game is rendered inside an HTML5 `<canvas>` element.

JavaScript handles the main game loop using:

```javascript
requestAnimationFrame(update);
```

The loop updates the game state, applies physics, moves objects, detects collisions and redraws the scene.

### Player Physics

The player's vertical movement is controlled using velocity and gravity.

```javascript
player.dy += player.gravity;
player.y += player.dy;
```

Jumping applies an upward velocity:

```javascript
player.dy = player.jumpPower;
```

Gravity then continuously pulls the player back toward the ground.

### Procedural Obstacles

Instead of using one completely fixed level, game objects are periodically generated during gameplay.

The game creates:

* Obstacles
* Moving platforms
* Portals

This keeps the game moving continuously while providing changing challenges.

### Cube Mode

The default gameplay mode behaves like a Geometry Dash-style cube.

The player:

* Automatically moves through the level
* Jumps over obstacles
* Rotates while airborne
* Lands on the ground and platforms

### 🚀 Rocket Mode

The game also includes a separate rocket player sprite and gameplay mode.

When in rocket mode, pressing **Space** or clicking affects the player's vertical velocity, creating a different movement style from normal cube jumping.

### 🏆 High Score

The highest score is stored using the browser's `localStorage`.

```javascript
localStorage.setItem("highScore", highScore);
```

This allows the high score to remain available even after refreshing or reopening the page in the same browser.

## 🚀 Running the Game

No installation or build process is required.

### Option 1 — Open Directly

Clone the repository:

```bash
git clone https://github.com/maharsh1580/geometry-dash-clone.git
```

Enter the directory:

```bash
cd geometry-dash-clone
```

Then open:

```text
index.html
```

in a modern web browser.

### Option 2 — Local Development Server

If Python is installed, you can start a simple local server:

```bash
python -m http.server 8000
```

Then open the local server in your browser.

## 🎯 Concepts Demonstrated

This project demonstrates several fundamental game-development concepts:

* Game loops
* 2D rendering
* Canvas graphics
* Basic physics simulation
* Velocity and gravity
* Collision detection
* Procedural object generation
* Sprite rendering
* Player input handling
* Game state management
* Particle effects
* Persistent browser storage

## 🔮 Possible Improvements

Future versions could include:

* Designed levels instead of only randomized generation
* Multiple difficulty levels
* Sound effects and background music
* Start/settings menu
* Mobile touch controls
* More portal types
* Additional player modes
* Better collision detection
* Level progression
* Speed-changing portals
* Improved animations
* Custom level editor
* Leaderboard system
* Modular JavaScript files instead of a single HTML file

## ⚠️ Disclaimer

This is a fan-made educational project inspired by the gameplay style of **Geometry Dash**.

It is not affiliated with or endorsed by the original game's developers or publishers.

## 👨‍💻 Author

**Maharsh Badheka**

GitHub: `@maharsh1580`

---

⭐ If you like the project, consider giving the repository a star!

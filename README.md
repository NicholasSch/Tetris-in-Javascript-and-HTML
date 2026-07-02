# 🧱 TETRISOW — HTML5 Outer Wilds Tetris Engine

A fully functional, modern reconstruction of the classic tile-matching puzzle game *Tetris*, completely themed around the indie video game *Outer Wilds*. 

This repository contains both a **ready-to-play client-side web deployment file** and the **full source code project space** for developers looking to modify or study the codebase.

---

## 📄 Project Overview

This implementation focuses on classic Tetris mechanics translated into an explicit event-driven JavaScript architecture over highly responsive HTML5 canvases. The game tracks a 10x20 structural logic grid. As random polyomino shapes (Tetrominos) drop into the active view matrix, players must position and rotate them to form solid horizontal lines. Clearing rows triggers point accumulation and updates global board states, while letting blocks stack to the upper boundary triggers a definitive game-over sequence that securely serializes high scores to browser state memory.

### Core Architecture Features
* **Multi-Canvas Presentation Framework:** Splits user interface concerns into three decoupled `<canvas>` viewports (Stats Dashboard, Active Gameplay Board, and Queue Preview Panel) to optimize frame updates.
* **Deterministic Event Loop:** Uses a precise execution loop driven by `requestAnimationFrame` to manage block gravity and input polling down to millisecond intervals.
* **Advanced Audio Loop Engine:** Combines custom sound effect hooks with an automated playlist system that shuffles and plays ambient sound layers directly from local source collections.

---

## 📂 Project Architecture

The core project assets, configurations, and ready-to-run files are organized into the following directory structure:

```text
TETRISOW/
│
├── index.html                      # 🚀 Unified Core Application & Interface File
│
└── Audio/                          # 🎵 Ambient soundtrack layers & sound effects
    ├── 14.3 billion years.mp3
    ├── main title.mp3
    ├── outer wilds-reprise.mp3
    ├── timber hearth.mp3
    ├── travelers.mp3
    ├── peca travada.mp3            # Block locking sound effect
    ├── pecamexeu.mp3               # Block movement sound effect
    └── line clear.mp3              # Row clear sound effect
```

---

## 🎮 Game Controls & Mechanics

The game architecture samples standard machine hardware keyboard mappings during active gameplay loops:

* ⬅️ / ➡️ **Left / Right Arrow Keys:** Shifts the active Tetromino horizontally across the grid coordinate boundaries.
* ⬆️ / **`Z` Key:** Rotates the moving piece 90° clockwise, executing bounding box checks to prevent boundary clipping through walls.
* ⬇️ **Down Arrow Key (Soft Drop):** Speeds up gravity temporarily, awarding +1 bonus point per row dropped.
* ⎵ **Spacebar (Hard Drop):** Instantly drops and locks the active block onto the lowest available valid grid coordinates, refreshing data statistics immediately and awarding +2 bonus points per row dropped.

---

## 🚀 How to Play & Run the Project

### Option A: Play Instantly (No Installation Required)
You do not need to download or install any specific compiler toolchains to play the game. The application is ready to play directly through any web browser:
1. Clone or download this repository folder layout as a `.zip` file to your local machine.
2. Open the root directory folder.
3. Double-click `index.html` (or open it with Google Chrome, Mozilla Firefox, Microsoft Edge, or Apple Safari) to launch and play immediately!

### Option B: Open Source Code (For Developers Only)
If you want to tweak, edit, or rebuild the JavaScript mechanics, layout styles, or canvas calculations from scratch:
1. Open the root `index.html` file inside your preferred code editor (such as VS Code or Sublime Text).
2. Modify the structural HTML5 canvas elements, tweak CSS background parameters, or update game rules directly inside the main `<script>` tag.
3. Save the file and simply refresh your open web browser tab to view your structural updates running live in real-time.

---

## ⚖️ Rights & Disclaimer

This project is a non-commercial, fan-made creation developed for educational and portfolio purposes. 
* I do not own any rights to the official soundtracks, musical themes, or background wallpapers from *Outer Wilds* used in the creation of this game. 
* All intellectual property, assets, trademarks, and copyrights belong entirely to Mobius Digital and Annapurna Interactive.

---

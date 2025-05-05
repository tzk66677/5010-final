# 5010-final
# Interactive Tree Growth & Weather Simulation

This p5.js project simulates a dynamic tree growth system with integrated weather effects and interactive pruning.

## Features

- **Tree Growth**
  - Branches grow from a central trunk
  - Random generation of **1–3** child branches with a minimum angle difference to avoid overlap
  - Growth stops near left, right, and top edges
  - Branches can be pruned by clicking and dragging ("scissors" cursor)

- **Weather System**
  - **Sunny**: Faint background image (`zen.png`) + rotating sun icon
  - **Rainy**: Blue-gray background + falling rain drops without trailing
  - **Snowy**: Light lavender background + bright, high-contrast snowflakes
  - Particle counts: rain (5 per frame), snow (2 per frame)

- **Background Image**
  - `zen.png` is center-cropped and rendered at low opacity (20/255)

- **Controls**
  - **1** – Switch to **Sunny**
  - **2** – Switch to **Rain**
  - **3** – Switch to **Snow**
  - **Space** – Reset tree to initial state
  - **Click & Drag** – Prune branches (scissors icon appears while dragging)

## Setup & Usage

1. **Dependencies**
   - [p5.js](https://p5js.org/) (include in HTML via CDN or local)
   - Place `zen.png` in the project root

2. **File Structure**
   ```
   /project
   ├── index.html         # loads p5.js and sketch.js
   ├── sketch.js          # main simulation code
   ├── zen.png            # background image
   └── README.md          # this file
   ```

3. **Running the Project**
   - Open `index.html` in a modern browser
   - Use the keys and mouse to interact

## Code Overview

- **sketch.js** contains:
  - `preload()` – loads the background image
  - `setup()` – initializes canvas and resets tree
  - `draw()` – main loop calling:
    - `drawBackground()`
    - `drawWeather()`
    - `updateTree()`
    - `updateWeather()`
  - Utility functions for branch growth, pruning, and collision detection

## Customization

- Adjust **growthSpeed**, **MAX_DEPTH**, **MAX_CHILDREN** in `sketch.js` to tweak tree complexity
- Change **weather particle** counts or styles in `drawWeather()` & `updateWeather()`
- Modify **tint** value in `drawBackground()` for different background opacity

---

Enjoy experimenting with procedural tree growth and weather dynamics!

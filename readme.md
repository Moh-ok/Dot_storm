# 🎯 DotStorm

**DotStorm** is a fast-paced browser arcade shooter built using **Vanilla JavaScript + HTML5 Canvas**.
Check out the live game [Dotstorm](https://dot-storm.vercel.app/).

You control a small player at the center of the screen while colorful enemy particles continuously spawn from all directions and move toward you.

Your mission:

> **Destroy the swarm before it reaches you.**

The game focuses on reflexes, aiming accuracy, and satisfying particle destruction effects.

---

## 🕹️ Gameplay

* The player remains at the center of the screen.
* Enemies spawn from the edges of the screen.
* They constantly move toward the player.
* Click anywhere to fire a projectile in that direction.
* Small enemies die in 1 hit.
* Bigger enemies require multiple hits.
* Large enemies shrink and scatter into particles when damaged.
* The game ends when any enemy touches the player.

**Goal:** survive as long as possible and achieve the highest score.

---

## ✨ Features

* HTML5 Canvas rendering
* Real-time shooting mechanics
* Particle explosion effects
* Enemy health based on size
* Continuous enemy spawning
* Smooth animations using `requestAnimationFrame`
* Fully written in pure JavaScript (no libraries or frameworks)

---

## 📁 Project Structure

```
dotstorm
│
├── package.json        (not required for gameplay)
├── app.js              (ignored in deployment)
├── .gitignore
├── README.md
│
└── public
      ├── index.html
      │
      └── js
           ├── index.js
           ├── eventlistener.js
           │
           └── classes
                ├── player.js
                ├── projectile.js
                ├── enemy.js
                └── particle.js
```

### File Responsibilities

| File               | Purpose                              |
| ------------------ | ------------------------------------ |
| `index.html`       | Canvas and main page                 |
| `index.js`         | Main animation loop & enemy spawning |
| `eventlistener.js` | Mouse input & shooting               |
| `player.js`        | Player rendering                     |
| `projectile.js`    | Bullet physics                       |
| `enemy.js`         | Enemy movement & behavior            |
| `particle.js`      | Explosion particles                  |

---

## ⚙️ Technical Overview

### Game Loop

The game runs a continuous animation loop:

```
requestAnimationFrame()
```

Every frame:

* Clears canvas
* Draws player
* Updates bullets
* Updates enemies
* Checks collisions
* Creates particles

---

### Collision Detection

Distance is calculated using:

```
distance = √((x2 - x1)² + (y2 - y1)²)
```

Used to detect:

* bullet → enemy hit
* enemy → player hit (game over)

---

### Enemy Health System

| Enemy Size | Hits Required |
| ---------- | ------------- |
| Small      | 1             |
| Medium     | 2–3           |
| Large      | 3–4           |

When hit, large enemies shrink until destroyed.

---

### Particle Effects

When an enemy is hit:

* dozens of particles spawn
* each particle has velocity
* friction slows movement
* opacity fades over time

This creates the colorful explosion effect.

---

## 🚀 Running the Game Locally

No installation needed.

### Method 1 — Direct

1. Clone the repository:

```
git clone https://github.com/YOUR-USERNAME/dotstorm.git
```

2. Open the project:

```
cd dotstorm/public
```

3. Open `index.html` in your browser.

---

### Method 2 — VS Code (Recommended)

1. Open the project in VS Code
2. Install **Live Server** extension
3. Right click `public/index.html`
4. Click **Open with Live Server**

---

## 🌐 Play Online

Hosted using GitHub Pages:

```
https://YOUR-USERNAME.github.io/dotstorm/
```

---

## 🎮 Controls

| Action | Input      |
| ------ | ---------- |
| Aim    | Move mouse |
| Shoot  | Left Click |

---

## 🧠 What This Project Demonstrates

* Object-oriented JavaScript
* Canvas animations
* Collision detection
* Event handling
* Game loops
* Modular file organization

---

## 🔮 Possible Future Improvements

* High score saving (localStorage)
* Sound effects
* Power-ups
* Pause / restart screen
* Mobile touch controls
* Difficulty scaling

---

If you like the project, consider giving it a ⭐ on GitHub!

# 🚀 Projectile Motion: Master Class & Orbital Arc Simulator

A dual-purpose web application that combines a physics educational module with a high-fidelity, gamified projectile motion simulator. Built entirely in a single HTML file using HTML5 Canvas, CSS3, and Vanilla JavaScript.

![Project Status](https://img.shields.io/badge/Status-Active-success)
![Tech](https://img.shields.io/badge/Tech-HTML%20%7C%20CSS%20%7C%20JS-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📖 Overview

This project is designed to teach and test the concepts of **Kinematics** and **2D Vector Motion**.
1.  **The Master Class:** A scrollable educational section explaining definitions, vectors, and the 7 key kinematic equations.
2.  **Orbital Arc (The Game):** An interactive lab where users launch projectiles on different planets, dealing with variable gravity, wind resistance, and atmospheric drag.

---

## ✨ Features

### 🎓 Educational Module
* **Visual Vector Breakdown:** Explains how velocity splits into $V_x$ and $V_y$ components.
* **Formula Grid:** Quick reference cards for calculating Range, Max Height, Time of Flight, etc.
* **Video Library:** Placeholders for educational embeds (CrashCourse, Professor Dave).

### 🎮 Orbital Arc Simulator
* **4 Unique Environments:**
    * 🌍 **Earth:** Standard gravity ($9.8 m/s^2$), mild wind.
    * 🌑 **Luna (Moon):** Low gravity ($1.6 m/s^2$), no air resistance (vacuum).
    * 🔴 **Mars:** Medium gravity ($3.7 m/s^2$), heavy variable winds.
    * 🪐 **Titan:** Low gravity ($1.35 m/s^2$) but very dense atmosphere (high drag).
* **Real-Time Telemetry:** Live readout of Altitude, Distance to Target, and Velocity.
* **Vector Visualization:** Toggle real-time velocity vector arrows (Green for X, Red for Y) during flight.
* **Time Dilation:** Control simulation speed (1.0x Real, 0.5x Slow, 0.2x Matrix Mode).
* **Progression System:** Earn ranks (Cadet to Legend) and unlock visual skins for the projectile based on win streaks.
* **"Earn Your Hint" System:** Unlock a trajectory prediction line by solving a physics math problem based on current environmental variables.

---

## 🛠️ How to Run

Since the project is contained within a single file, no build process or server installation is required.

1.  **Download** the code.
2.  Save the file as `index.html`.
3.  **Open** the file in any modern web browser (Chrome, Firefox, Edge, Safari).

---

## 🕹️ How to Play

1.  **Select Environment:** Click a planet card on the title screen to initialize the physics engine with that planet's gravity and atmosphere.
2.  **Aim & Fire:**
    * Adjust **Angle** slider ($0^\circ - 90^\circ$).
    * Adjust **Force** slider (Initial Velocity).
    * Click **LAUNCH**.
3.  **The Objective:** Land the projectile within the red target zone.
    * *Hit:* You gain a streak point and rank progress.
    * *Miss:* Streak resets. Analyze the "Status Report" to adjust your next shot.
4.  **Using Hints:**
    * If you have battery charge (you start with 3), click **HINT**.
    * Solve the physics question presented (e.g., Calculate Vertical Velocity).
    * If correct, a trajectory line will appear to guide your aim.

---

## 🧮 The Physics Engine

The simulation uses a custom JavaScript physics loop running at 60 FPS (modified by the time scale).

**Key Calculations Used in Code:**
* **Drag:** Calculated as a simplified coefficient based on velocity: `drag = air_density * velocity`
* **Acceleration X:** `ax = -(drag * vx) + wind_force`
* **Acceleration Y:** `ay = -(drag * vy) + gravity`
* **Euler Integration:** Used to update position and velocity every frame.

---

## 🎨 Customization

You can easily modify the game by editing the `<script>` section inside `index.html`:

* **Change Planets:** Edit the `PLANETS` constant array to add new worlds (e.g., Jupiter with high gravity).
* **Adjust Difficulty:** Change the target radius in `gameState.target.r`.
* **Modify Questions:** Add new math problems to the `QUESTION_TYPES` array.

## 📂 File Structure

The code is a "Monolith" (Single File Component):
* **CSS:** Located in `<style>`, handles the dark "Tech/Space" UI theme, animations, and modal layouts.
* **HTML:** Structure for the educational content and the game UI wrapper.
* **JS:** Located in `<script>`, handles the Canvas drawing, physics loop, game logic, and DOM manipulation.

---
*Created for the Orbital Arc Project.*

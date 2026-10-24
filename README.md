<div align="center">

  <h1>∞ MORPHOS</h1>

  <p>
    <b>Interactive Desk Clock, 3D Split-Flap Timepiece & Pomodoro Focus Studio</b><br/>
    <sub>A distraction-free clock and study companion with interactive canvas physics, 18 themes, and real-time audio synthesis — all in a single HTML file.</sub>
  </p>

  <p>
    <a href="https://ysharf.github.io/Timer/">
      <img src="https://img.shields.io/badge/LIVE_DEMO-OPEN_CLOCK-9C8AE8?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=0d1117" alt="Live Demo" />
    </a>
    <img src="https://img.shields.io/badge/MODES-MORPHOS_%7C_3D_FLIP_%7C_DIGITAL-75DCD0?style=for-the-badge&labelColor=0d1117" alt="Modes" />
    <img src="https://img.shields.io/badge/DEPENDENCIES-ZERO_(1_FILE)-C9CED8?style=for-the-badge&labelColor=0d1117" alt="Zero Dependencies" />
  </p>

  <p>
    <a href="https://ysharf.github.io/Timer/"><b>Live Demo</b></a> ·
    <a href="#display-engines">Display Engines</a> ·
    <a href="#interactive-physics">Interactive Physics</a> ·
    <a href="#focus--time-suite">Focus Suite</a> ·
    <a href="#shortcuts">Shortcuts</a> ·
    <a href="#العربية"><b>العربية</b></a>
  </p>

</div>

---

## Overview

**MORPHOS ∞** combines three distinct clock styles—a physics-driven mathematical canvas clock, a classic 3D mechanical flip clock, and a clean digital display—into one lightweight web app.

It is built inside a single, dependency-free `index.html` file so it loads instantly, works offline, and stays awake on secondary monitors, tablets, and mobile phones during long study or work sessions.

---

## Display Engines

Switch between three rendering engines at any time by pressing <kbd>D</kbd>:

| Engine | Architecture | Description |
| :--- | :--- | :--- |
| **MORPHOS ∞** | **HTML5 Canvas + Spring Physics** | Digits (`0–9`) are drawn as continuous cubic Bézier curves with internal tension strings. On every tick, numbers physically unfold and morph into the next digit. |
| **3D Split-Flap** | **CSS 3D Transforms** | Mechanical split-flap cards with realistic depth shadows, hinge notches, and an optional synthesized flip tick sound. |
| **Minimal Digital** | **Tabular Typography** | High-contrast numerals (`Inter`, `Oswald`, `JetBrains Mono`, `Space Grotesk`) with smooth settle animations and `Pure`, `Glass`, or `Neon` styles. |

---

## Interactive Physics

When using **MORPHOS ∞** mode, the digits respond directly to your mouse or touch:

* **Mouse & Touch Field (`Attract` / `Repel`):** Moving your cursor or swiping a finger across the clock bends and warps the Bézier curves in real time, reacting to your movement speed and direction changes.
* **Pluckable Strings:** Every digit has internal tension chords that you can grab, pull, and release like guitar strings. Releasing a chord triggers harmonic vibration and a **Web Audio string pluck** scaled to how hard you pulled it.
* **Cross-Digit Sparks:** When a number changes, energy sparks travel along its curves and jump across the separators into neighboring digits.
* **Background Astrolabe:** A subtle geometric circle behind the clock tracks your current minute or timer progress and etches small runic marks as you finish focus sessions, tasks, or laps.

---

## Focus & Time Suite

| Tool | Features |
| :--- | :--- |
| **Wall Clock** | 12-hour or 24-hour format with optional seconds, weekday, and date display. |
| **Quick Timer** | 16 ready-made presets (`15s` to `60m`) plus custom hours, minutes, and seconds input. |
| **Study Timer (Pomodoro)** | Freely customizable Focus, Short Break, and Long Break durations (up to `360m`), quick presets (`10m`–`90m`), and automatic session tracking. |
| **Stopwatch** | `10ms` precision stopwatch with split and lap history table. |
| **Countdown** | Target date and time countdown that saves automatically in your browser. |

### Built for Deep Work
* **Procedural Task Sigils:** Each task you add in Study Mode generates a unique geometric icon from its title. Completing focus sessions progressively lights up segments of the icon.
* **Built-In Study Soundscape:** Generates background focus audio in real time using the Web Audio API (no external audio files needed), including an **Euclidean Rhythm** pulse generator, a warm **Ambient Drone**, and an optional **Binaural Offset**.
* **Clean Fullscreen & Always-On Screen:** Double-click (or double-tap on mobile) anywhere on the background to hide all buttons (`0%` opacity) and keep your screen awake on mobile, tablet, or desktop.

---

## Shortcuts

| Key / Gesture | Action |
| :---: | :--- |
| <kbd>Space</kbd> | Start or Pause the active Timer, Study session, or Stopwatch |
| <kbd>D</kbd> | Cycle between `MORPHOS ∞`, `3D Flip`, and `Digital` modes |
| <kbd>F</kbd> or <kbd>Double-Tap</kbd> | Toggle **Clean Fullscreen Mode** (hides all UI controls 100%) |
| <kbd>Esc</kbd> | Exit Fullscreen or close any open menu |

---

## Run Locally

No installation or build tools needed. Clone the repo and open `index.html` in any browser:

```bash
git clone https://github.com/ysharf/Timer.git
cd Timer

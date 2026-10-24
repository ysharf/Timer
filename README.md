# MORPHOS ∞ / Flip Clock

**Live Demo:** [https://ysharf.github.io/Timer/](https://ysharf.github.io/Timer/)

A standalone desk clock, Pomodoro focus timer, and stopwatch built entirely inside a single, dependency-free `index.html` file.

Designed to run smoothly on desktop monitors, tablets, and mobile phones without the screen dimming, and without needing a build step or external audio files.

---

### Features

#### 1. Three Display Engines (Press `D` to switch)
* **MORPHOS ∞:** A 60fps HTML5 Canvas engine where digits (`0–9`) are drawn as continuous cubic Bézier splines with internal tension chords and runic anchors. Instead of swapping text on each tick, digits physically morph into the next number using spring-damper physics.
* **3D Split-Flap:** Classic mechanical flip cards built with CSS 3D transforms, perspective shadows, and an optional synthesized mechanical tick.
* **Minimal Digital:** Clean tabular numerals with four font options (`Inter`, `Oswald`, `JetBrains Mono`, `Space Grotesk`) and subtle settle animations.

#### 2. Interactive Canvas Physics (Morphos Mode)
* **Touch & Mouse Vector Field:** Moving the mouse or swiping your finger across the digits pulls or repels the Bézier curves in real time, with velocity wake and recoil when reversing direction.
* **Pluckable Harmonic Chords:** The internal tension strings inside each digit can be grabbed and plucked with the mouse or finger. Releasing a string triggers damped harmonic oscillation and a Web Audio string pluck scaled to the pull tension.
* **Cross-Digit Sparks:** When a digit changes, energy packets travel along its spine and leap across the separators into neighboring digits.
* **Background Astrolabe:** A geometric circle behind the clock tracks active progress and permanently etches small runic seals as you complete focus sessions, tasks, or stopwatch laps.

#### 3. Focus & Time Suite
* **5 Core Modes:**
  * **Clock:** 12h / 24h wall clock with optional seconds and date display.
  * **Timer:** 16 quick presets (15s to 60m) + custom hours/minutes/seconds input.
  * **Study (Pomodoro):** Fully customizable focus, short break, and long break durations (up to 360 minutes) with quick presets (`10m` to `90m`).
  * **Stopwatch:** 10ms resolution chronometer with split/lap recording table.
  * **Countdown:** Target date/time event countdown with persistent storage.
* **Procedural Task Sigils:** Every task added in Study Mode generates a deterministic SVG sigil from its name. Each completed focus session lights up one segment of the sigil until the task is complete.
* **Real-Time Web Audio Soundscape:** All chimes, string plucks, and study background audio (Euclidean rhythm generator, ambient harmonic drone, and binaural stereo offset) are synthesized in real time using the native Web Audio API—zero `.mp3` assets.
* **Local Analytics:** Tracks daily focus goals, day streaks, and 7-day / 30-day / 12-month bar charts in `localStorage` with one-click CSV export.

#### 4. Mobile & Tablet Ready
* ** Distraction-Free Fullscreen:** Double-click (or double-tap on mobile) anywhere on the background to enter clean fullscreen mode, where all toolbars and buttons completely vanish (`0%` opacity), leaving only the timepiece on screen.
* **Triple-Layer Screen Wake Lock:** Uses the native Screen Wake Lock API, a visibility watchdog, and an offscreen `2x2` canvas video stream so mobile and tablet browsers (Android Chrome / Samsung Tab / iOS) never put the screen to sleep.
* **18 Curated Themes:** 16 dark/OLED palettes and 2 light palettes.

---

### Controls & Shortcuts

| Shortcut / Gesture | Action |
| :--- | :--- |
| `Space` | Start / Pause active Timer, Study session, or Stopwatch |
| `D` | Cycle between `Morphos ∞`, `3D Flip`, and `Digital` |
| `F` or `Double-Tap` | Toggle Clean Fullscreen mode |
| `Esc` | Exit Fullscreen or close open drawers/modals |

---

### Running Locally

No dependencies or build tools required. Clone the repository and open `index.html` directly in any browser:

```bash
git clone https://github.com/ysharf/Timer.git
cd Timer

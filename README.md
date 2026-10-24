# MORPHOS ∞ / Flip Clock

**Live Demo:** [https://ysharf.github.io/Timer/](https://ysharf.github.io/Timer/)

A standalone desk clock and focus timer built inside a single, dependency-free `index.html` file. 

I wanted a clean timepiece and Pomodoro setup that I could leave running on a secondary monitor or tablet (specifically tested on a Samsung Galaxy Tab A9+) without the screen dimming, and without needing a build step or external audio files.

---

### What's Inside

#### 1. Three Display Engines (Press `D` to switch)
* **MORPHOS ∞:** A 60fps HTML5 Canvas engine where digits (`0-9`) are drawn as continuous cubic Bézier splines with internal tension chords and runic anchors. Instead of swapping text on each tick, digits physically morph into the next number using spring-damper physics.
* **3D Split-Flap:** Classic mechanical flip cards built with CSS 3D transforms, perspective shadows, and an optional synthesized mechanical tick.
* **Minimal Digital:** Clean tabular numerals with four font options (`Inter`, `Oswald`, `JetBrains Mono`, `Space Grotesk`) and subtle settle animations.

#### 2. Interactive Canvas Physics (Morphos Mode)
* **Cursor Field:** Moving the mouse or dragging a finger across the digits pulls or repels the Bézier curves in real time, with velocity wake and recoil when reversing direction.
* **Pluckable Chords:** The internal tension strings inside each digit can be grabbed and plucked with the mouse. Releasing a string triggers damped harmonic oscillation and a Web Audio string pluck scaled to the pull tension.
* **Cross-Digit Sparks:** When a digit changes, energy packets travel along its spine and leap across the separators into neighboring digits.
* **Background Astrolabe:** A geometric circle behind the clock tracks current progress and permanently etches small runic seals as you complete focus sessions, tasks, or stopwatch laps.

#### 3. Focus & Time Tools
* **5 Modes:** Wall Clock, Countdown Timer (16 presets + custom time), Pomodoro Study Timer, Stopwatch (10ms resolution + split laps), and Date/Time Countdown.
* **Procedural Task Sigils:** Every task added in Study Mode generates a deterministic SVG sigil from its name. Each target Pomodoro lights up one segment of the sigil until the task is complete.
* **Web Audio Soundscape:** All chimes, string plucks, and study background audio (Euclidean rhythm generator, harmonic drone, and binaural offset) are synthesized in real time using the native Web Audio API—zero `.mp3` assets.
* **Local Analytics:** Tracks daily focus goals, streaks, and 7-day / 30-day / 12-month history in `localStorage` with CSV export.

#### 4. Tablet Keep-Awake & Themes
* **Always-On Screen:** Uses a 3-layer wake lock (Native Screen Wake Lock API + visibility watchdog + a hidden 2x2 canvas video stream) so mobile/tablet browsers like Android Chrome never put the screen to sleep.
* **18 Themes:** 16 dark/OLED themes and 2 light themes, plus auto-hiding UI controls after 3 seconds of inactivity.

---

### Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `Space` | Start / Pause active Timer, Study session, or Stopwatch |
| `D` | Cycle between `Morphos ∞`, `3D Flip`, and `Digital` |
| `F` | Toggle Fullscreen (or double-click anywhere on the background) |
| `Esc` | Close open drawers or modals |

---

### Running Locally

No dependencies or build tools required. Just clone the repo and open `index.html` in any browser:

```bash
git clone https://github.com/ysharf/Timer.git
cd Timer

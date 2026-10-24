<div align="center">

  <a href="https://ysharf.github.io/Timer/">
    <img src="https://wsrv.nl/?url=https://github.com/user-attachments/assets/89fb7a4f-0ddb-4d1c-ad11-b5e2636f84b7&w=160&h=160&fit=cover&mask=circle&output=png" width="96" height="96" alt="MORPHOS ∞" />
  </a>

  <h1>MORPHOS ∞</h1>

  <p>
    <b>Living Mathematical Timepiece, 3D Split-Flap Clock & Pomodoro Focus Studio</b><br/>
    <sub>Built entirely inside a single, zero-dependency HTML file with real-time spring physics & Web Audio synthesis.</sub>
  </p>

  <p>
    <a href="https://ysharf.github.io/Timer/">
      <img src="https://img.shields.io/badge/LIVE_DEMO-LAUNCH_APP-9C8AE8?style=for-the-badge&logo=googlechrome&logoColor=white&labelColor=0d1117" alt="Live Demo" />
    </a>
    <img src="https://img.shields.io/badge/ENGINE-60FPS_CANVAS_%2B_CSS_3D-75DCD0?style=for-the-badge&labelColor=0d1117" alt="Engine" />
    <img src="https://img.shields.io/badge/AUDIO-WEB_AUDIO_SYNTH-C9CED8?style=for-the-badge&labelColor=0d1117" alt="Audio" />
  </p>

  <p>
    <a href="https://ysharf.github.io/Timer/"><b>Live Demo</b></a> ·
    <a href="#display-engines">Display Engines</a> ·
    <a href="#interactive-physics">Physics</a> ·
    <a href="#focus--time-suite">Focus Suite</a> ·
    <a href="#shortcuts">Shortcuts</a> ·
    <a href="#العربية"><b>العربية</b></a>
  </p>

</div>

<br/>

---

## Display Engines

Switch seamlessly between three distinct rendering engines at any time by pressing <kbd>D</kbd>:

| Engine | Rendering Architecture | Visual Character |
| :--- | :--- | :--- |
| **MORPHOS ∞** | **HTML5 2D Canvas + Spring Physics** | Digits (`0–9`) are constructed from connected cubic Bézier spines, counter-manifolds, and elastic tension chords that physically unfold and morph into the next number. |
| **3D Split-Flap** | **Hardware-Accelerated CSS 3D** | Classic mechanical split-flap cards with perspective depth shadows, hinge notches, and optional synthesized mechanical tick audio. |
| **Minimal Digital** | **Tabular Typography Engine** | High-contrast numerals (`Inter`, `Oswald`, `JetBrains Mono`, `Space Grotesk`) with per-digit settle animations and `Pure`, `Glass`, or `Neon` framing. |

---

## Interactive Physics

In **MORPHOS ∞** mode, the clock is a live physical simulation rather than a pre-rendered animation:

* **Cursor & Touch Vector Field (`Attract` / `Repel`):** Moving your mouse or swiping your finger across the digits warps the Bézier control handles in real time using a smooth $C^2$ falloff curve, complete with velocity wake and recoil when reversing direction.
* **Pluckable Harmonic Chords:** Each digit contains internal tension strings that can be grabbed and pulled taut with your mouse or finger. Releasing a chord triggers damped harmonic oscillation and a **Web Audio string pluck** whose pitch bend and brightness scale with your pull tension.
* **Cross-Digit Spark Coupling:** When a digit changes, arcane energy packets travel along its spine and leap across the geometric separators into neighboring digits.
* **Living Astrolabe Seal:** The geometric astrolabe behind the clock tracks active progress and permanently etches small runic seals as you complete focus sessions, tasks, and stopwatch laps.

---

## Focus & Time Suite

| Mode | Capabilities |
| :--- | :--- |
| **Clock** | 12-hour / 24-hour wall clock with optional seconds manifold, weekday, and calendar date. |
| **Timer** | 16 calibrated quick presets (`15s` to `60m`) + custom hours, minutes, and seconds input. |
| **Study (Pomodoro)** | Fully customizable Focus, Short Break, and Long Break durations (up to `360m`), quick presets (`10m`–`90m`), and automatic session logging. |
| **Stopwatch** | `10ms` precision chronometer with split duration and total elapsed lap table. |
| **Countdown** | Target date & time horizon countdown with persistent browser storage. |

### Built-In Study Tools
* **Procedural Task Sigils:** Adding a task in Study Mode hashes its name into a unique geometric SVG sigil. Each completed focus session illuminates one segment of the sigil until the task is complete.
* **Generative Web Audio Soundscape:** Synthesized 100% in real time with zero external `.mp3` files—featuring an **Euclidean Rhythm Generator** $(k, n)$, an **Ambient Harmonic Drone**, and an optional **Binaural Stereo Offset**.
* **Mobile & Tablet Keep-Awake:** Uses a triple-layer wake lock (Native `navigator.wakeLock` + visibility watchdog + offscreen `2x2` canvas stream) so phones and tablets never dim during a study session.
* **18 Curated Themes:** 16 Dark / OLED themes and 2 Light themes, plus **Clean Fullscreen Mode** where all UI controls vanish completely (`0%` opacity).

---

## Shortcuts

| Key / Gesture | Action |
| :---: | :--- |
| <kbd>Space</kbd> | Start / Pause active Timer, Study session, or Stopwatch |
| <kbd>D</kbd> | Cycle Display Engine (`MORPHOS ∞` → `3D Flip` → `Digital`) |
| <kbd>F</kbd> or <kbd>Double-Tap</kbd> | Toggle **Clean Fullscreen Mode** (hides all UI 100%) |
| <kbd>Esc</kbd> | Exit Fullscreen or close open drawers and modals |

---

## Quick Start

The entire application is self-contained inside `index.html`. No build step or dependencies required:

```bash
git clone https://github.com/ysharf/Timer.git
cd Timer
# Open index.html in any browser

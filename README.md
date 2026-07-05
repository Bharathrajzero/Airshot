# AirShot

AirShot is a futuristic, browser-based arcade shooting gallery powered by computer vision. Players use physical air gestures captured via a standard webcam to control a virtual laser reticle and smash moving neon bottles on an active conveyor belt grid[cite: 1]. 

Built completely with vanilla frontend technologies, MediaPipe Hands, and the dynamic Web Audio API, it features adaptive hand-tracking smoothing, low-latency crosshairs, and a fully synthetic retro sound design with zero dependencies on heavy asset files[cite: 1].

---
## Screenshot
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/dcac28fd-0ffc-406e-9a87-b022a4c02a6a" />
<img width="1920" height="1079" alt="image" src="https://github.com/user-attachments/assets/6c686eec-a292-419f-aa7d-5fc85168fbdb" />



## Live Features

* **Interactive Hand-Gesture Controls:** Track index fingertips in real-time to control the laser sight accurately using a customized MediaPipe processing pipeline[cite: 1].
* **Dual Trigger Modes:**
  * **Pinch-to-Shoot:** Touch your thumb and index finger together to trigger immediate firing actions (utilizes a dual-threshold Schmitt trigger to prevent misfires)[cite: 1].
  * **Hover-Lock:** Keep the crosshair locked over a bottle to auto-charge and deploy shots automatically[cite: 1].
* **Procedural Synth Sound Effects:** Implements native Web Audio API oscillators and gain nodes to generate retro laser sound effects, explosion booms, glass shattering rings, and reloads on-the-fly[cite: 1].
* **Dynamic Armory:** Choose between the rapid Laser Gun, wide-spread Shotgun, or high-scoring Railgun—each calibrated with discrete ammunition caps, custom reload times, and score multipliers[cite: 1].
* **Multiple Game Modes:**
  * **Conveyor Belt (Classic):** An infinite gallery mode prioritizing survival accuracy and combo streaks[cite: 1].
  * **Time Challenge (Survival):** A tense 60-second race against the clock where hitting specific bonus targets keeps the timer ticking[cite: 1].
* **Robust Fallback System:** Auto-detects blocked cameras and dynamically re-binds tracking schemas to localized mouse coordinates and touch layouts[cite: 1].

---

## Technology Stack

* **Core Engine:** HTML5 Canvas, Vanilla JavaScript (ES6+)[cite: 1]
* **Styles and Theme:** Tailwind CSS, FontAwesome Icons, Google Fonts (Orbitron and Rajdhani)[cite: 1]
* **Computer Vision:** MediaPipe Hands API (@mediapipe/hands and @mediapipe/camera_utils)[cite: 1]
* **Audio Synthesizer:** Web Audio API (OscillatorNode, BiquadFilterNode, AudioBufferSourceNode)[cite: 1]

---

## Project Structure

```text
airshot/
│
├── neon_bottle_shooter.html  # Main application core file containing markup, style, and game logic
└── README.md                 # Project documentation and setup guide

```

---

## Quick Start Installation

No build steps or Node modules required. You can run this natively straight out of your browser.

1. Clone or download the repository to your desktop machine:
```bash
git clone [https://github.com/Bharathrajzero/Airshot.git](https://github.com/Bharathrajzero/Airshot.git)

```


2. Navigate into the folder:
```bash
cd Airshot

```


3. Open `neon_bottle_shooter.html` in any modern web browser (Google Chrome, Microsoft Edge, or Brave recommended for optimized MediaPipe sandboxing and camera access).

---

## How To Play

1. **Setup:** Position yourself roughly 2–3 feet away from your web camera lens in a well-lit space.


2. **Aim:** Raise either hand into the frame. The application will track your Index Fingertip to move the laser reticle across the grid.


3. **Shoot:**
* *Pinch Trigger Mode:* Touch your thumb and index finger together to fire.


* *Hover-Lock Mode:* Keep your target perfectly static over a bottle to build up an auto-fire sequence.




4. **Reload:** Press the R key on your physical keyboard, or pinch your fingers together outside the game window boundary to reload empty chambers.


5. **Score Guide:**
* **Neon Bottles:** Standard targets. Keep chains active to increase score multipliers (x1 to x8).


* **Golden Bonus Bottles:** Grants heavy points, multiplies your score, and restores weapon ammo instantly.


* **Toxic Poison Bottles:** Avoid these. Striking them reduces your total score and breaks your combo chain.





---

## Authors

* **Bharathrajzero** - *Initial Work and Architecture* - [GitHub Profile](https://www.google.com/search?q=https://github.com/Bharathrajzero)

---

## License

This project is licensed under the MIT License © 2026 Bharath Raj, AlphaGroup.

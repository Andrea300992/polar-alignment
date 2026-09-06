# Polar Alignment

Real-time polar alignment using your phone's GPS and orientation sensors — targets true Polaris or the South Celestial Pole.

A browser-based polar alignment tool that uses your phone's GPS, compass, and gyroscope to point at true Polaris (Northern Hemisphere) or the South Celestial Pole (Southern Hemisphere) in real time — no external polar scope required.

## Features

- **Real astronomical target**: computes Polaris' true altitude/azimuth from GPS position and current time (not just "north"), or the fixed South Celestial Pole position for the southern hemisphere.
- **Live crosshair display**: shows how far off you are from the target, with a color-coded quality indicator (red → green).
- **Compass calibration**: manually zero out compass drift/interference when you know you're pointed correctly.
- **Sensor (figure-8) calibration**: guided remagnetization step before pointing, plus automatic detection of magnetic interference during use, with a one-tap re-calibration prompt.
- **Auto hemisphere detection** from GPS latitude.

## Usage

1. Open `polar-align.html` in a mobile browser (see note below on HTTPS).
2. Grant location and motion/orientation sensor permissions when prompted.
3. Follow the figure-8 calibration prompt.
4. Hold the phone vertically (portrait), using the top edge as a sighting line toward the sky, and move it until the crosshair centers green.

## Important: HTTPS required

Device orientation and geolocation sensors only work in a **secure context** (HTTPS or localhost). Opening the file directly from local storage (`file://`) will likely not trigger permission prompts on iOS/Android.

The easiest way to serve it securely is via **GitHub Pages**:

1. Repo → Settings → Pages
2. Source: Deploy from a branch → `main` → `/ (root)`
3. Save, then open the generated `https://andrea300992.github.io/polar-alignment/polar-align.html` URL on your phone.

## Accuracy note

Precision is limited by phone sensor noise (typically ±1–2°). This tool is meant for **rough pre-alignment**, not a replacement for a physical polar scope or plate-solving for precision tracking.

## License

MIT

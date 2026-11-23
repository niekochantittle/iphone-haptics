# Inside the Buzz: How iPhone Haptics Work

**Global Virtual Hackathon 2026 – Theme: Unveiling Technology**

## The problem
Every day we feel our phones tap, thump and rumble, but few people know how. Haptics look like magic, and nobody explains them.

## What it does
An interactive web page that unveils the technology behind iPhone vibration:
- **Simulator**: change frequency, strength and duration and see the waveform and a shaking phone.
- **Game presets**: explosion, bullet hit, heartbeat, engine rumble, coin and low health.
- **Explainer**: how a linear resonant actuator (the Taptic Engine) works, and how it differs from old spinning motors.
- **Haptic designer**: draw a vibration pattern and export it as Core Haptics (AHAP) JSON for iPhone apps or Kotlin code for Android.
- **Quiz**: check what you learned.

## How it works
Single file: `iphone-haptics.html` (HTML, CSS, vanilla JavaScript, no libraries).
- The waveform is computed as amplitude × sin(2π · frequency · time), shaped by a strength envelope.
- Real vibration uses the browser Vibration API where supported (Android browsers). iPhone Safari does not allow it, so the page shows a visual simulation there.
- The AHAP export builds a Core Haptics `HapticContinuous` event for each 50 ms step with `HapticIntensity` and `HapticSharpness`.

## Run it
Open `iphone-haptics.html` in any browser. No install needed.

## Limits and next steps
- Web pages cannot trigger the iPhone Taptic Engine. A Swift app using Core Haptics would.
- Next: import AHAP files, add audio sync, add accessibility alert patterns.

## Team
(Add names, school, and supervising teacher here.)

## Credits
(List any tutorials, documentation or tools you used, including AI assistance if the rules ask for it.)

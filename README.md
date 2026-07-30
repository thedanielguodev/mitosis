# Mitosis: Cell Division

A small interactive lesson on mitosis. A-Frame handles the scene, everything else (the DNA helix, the mitochondria, the ATP particle burst) is hand-written Three.js instead of imported models.

Runs in a regular browser, on a phone, or in a VR headset with hand controllers.

## Running it

It's a single static HTML file, so any local server works:

```
python3 -m http.server 8000
```

Open `http://localhost:8000`. No build step, no dependencies to install.

## What's in it

You step through the five phases of mitosis with buttons or the dots along the bottom. Every part of the cell (chromosomes, spindle fibers, membranes, the mitochondria) can be clicked for a short explanation, and clicking the mitochondria fires a burst of ATP particles. During Interphase there's a rotating DNA double helix built from a custom Three.js curve rather than a loaded model.

There's a five-question quiz, one question per phase, with immediate feedback on each answer. A small progress bar in the corner tracks how many of the clickable parts you've actually found, and that persists across visits.

If you put on a headset, the hand controllers get laser pointers for clicking things, and the gaze cursor switches to dwell-to-click if there's no controller.

All the sound (phase transitions, the ATP pulse) is synthesized with the Web Audio API on the fly, so there are no audio files to load.

## Controls

- Buttons or dots at the bottom move between phases
- Click (or gaze / controller trigger) on anything highlighted
- The pad in the top right, or dragging to look, moves the camera
- "quiz" and "learning goal" in the top bar reopen those at any time

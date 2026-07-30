# Mitosis: Cell Division

An interactive WebXR lesson on mitosis, built with [A-Frame](https://aframe.io) and raw [Three.js](https://threejs.org). Walk through the five phases of cell division, click on parts of the cell to learn what they do, and take a quiz to check your understanding.

Works in a desktop browser, on mobile, and in VR headsets (Quest, Vive, etc.) with full hand-controller support.

## Run it

Any static file server works, e.g.:

```
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

## Features

- **5-phase walkthrough** — Interphase through Telophase & Cytokinesis, with animated chromosomes, spindle fibers, and membranes.
- **Click-to-learn** — every part of the cell (chromosomes, centromeres, spindle fibers, membranes, mitochondria) has its own explanation.
- **Procedural Three.js visuals** — a rotating DNA double-helix (custom `TubeGeometry` curve) during Interphase, a capsule-and-cristae mitochondria mesh, and a `THREE.Points` ATP particle burst on click — no 3D model assets required.
- **Knowledge-check quiz** — 5 questions, one per phase, with instant right/wrong feedback and a score summary.
- **Discovery tracker** — counts unique parts explored, persisted across visits via `localStorage`.
- **VR-ready** — laser-controls for hand controllers, dwell-to-click gaze cursor as a fallback in headsets without controllers.
- **Synthesized audio** — phase-transition and interaction sounds generated with the Web Audio API, no audio files.

## Controls

- **Buttons** at the bottom step through phases; the phase dots jump directly to one.
- **Click / gaze / controller trigger** on any highlighted part of the cell for an explanation.
- **Movement pad** (top right) or WASD-style drag-look to move around the scene.
- **quiz** / **learning goal** buttons (top bar) open the quiz or re-show the intro.

## Stack

Plain HTML/CSS/JS — no build step. A-Frame 1.7 + aframe-extras via CDN; all custom geometry and particle effects are hand-written Three.js.

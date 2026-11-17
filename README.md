# Glim

**Open it here: https://shrer488.github.io/Glim/**

A hand-tracking light toy for your webcam. Pinch your fingers, pull them apart, and a glowing band of light stretches across the gap like rubber, thinning as you pull and bouncing as you move. Moths fly in from the dark toward it.

## How to use it

1. Open the link above in Chrome, Edge or Safari on a computer with a webcam.
2. Click **Start camera** and allow camera access.
3. Pinch your thumb against a finger, then pull them apart to light a beam between them.
4. Make a fist to put the light out.

| Gesture | What it does |
|---|---|
| Pinch thumb + index, pull apart | Pink beam |
| Pinch thumb + middle, pull apart | Blue beam |
| Pinch thumb + ring, pull apart | Green beam |
| Pinch thumb + pinky, pull apart | Gold beam |
| Pinch another finger while a beam is on | Switch to that finger's color |
| Touch a fingertip to one on your other hand | Join both beams into a rectangle of light |
| Make a fist | Turn the light off |

No camera? Press and drag anywhere on the page to pull out a beam with your mouse.

## What you'll see

- Moths appear as photo negatives in the dark and turn into their true colors as they get close to the light.
- They fly in front of you and behind you, hidden by your body when they pass behind.
- The **Moths** slider sets how many there are, from 1 to 30. More moths means smaller moths.
- The colored dots on the little hand in the corner set each finger's beam color. Click one to change it.

Everything runs in your browser. Video from your camera is never uploaded anywhere.

## Run it on your own computer

Browsers only allow the camera on `https` pages or on `localhost`, so serve the folder instead of opening the file directly:

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173.

## How it's built

- One page, [index.html](index.html), with no build step.
- Hand tracking and body detection use Google's [MediaPipe](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker), loaded from a CDN.
- The moths in [moths/](moths/) are cut from photos, each split into a wings layer and a body layer so the wings can flap.

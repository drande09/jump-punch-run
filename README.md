# 🏃 Jump Punch Run! 🥊

A webcam motion-controlled endless runner for kids. Your body is the controller:

- **Jump** for real → your character jumps over rocks, boxes, cacti and holes
- **Punch** the air → your character punches monsters
- Stay in the camera view (the game pauses if you wander off!)
- Run as far as you can — it gets faster and harder as you go

Keyboard fallback: **Space** = jump, **P** or **X** = punch.

## How it works

- Pure static site — one `index.html`, no build step, no server.
- Pose tracking via [MediaPipe Pose Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/pose_landmarker) running 100% in the browser. Video never leaves the device.
- Jump detection: hips rising sharply above a slow-moving baseline.
- Punch detection: fast wrist snap or arm thrown out to the side.
- Sounds are synthesized with WebAudio (no assets).

## Run locally

Serve the folder over HTTP (camera access requires a secure context; `localhost` counts):

```
npx http-server -p 8080
```

## Play

Deployed on GitHub Pages: https://drande09.github.io/jump-punch-run/

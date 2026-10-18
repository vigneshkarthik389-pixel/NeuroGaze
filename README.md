# NeuroGaze
NeuroGaze: An opt-in webcam-assisted learning interface with experimental visual feedback signals 
# NeuroGaze Website Prototype


## Enable webcam mode
Camera access may be blocked from a `file://` URL. If so:
1. Install Python if needed.
2. Open a terminal in this folder and run `python -m http.server 8000`.
3. Visit `http://localhost:8000`, click **Start camera**, and allow camera permission.
Webcam mode loads MediaPipe from jsDelivr and requires internet access. Demo mode does not need a camera.

## Put it online
This is a static website. Deploy the folder with Netlify, import it into Vercel, or upload `index.html` to a GitHub Pages repository. Use HTTPS for camera permissions on a public website.

## Technical honesty
Live mode uses MediaPipe Face Mesh to estimate blink events, rough head direction, face position, and face movement. It does not perform calibrated eye-to-screen gaze tracking. The displayed dwell score is a heuristic, not a validated measure of cognitive load, confusion, or comprehension. Demo mode uses simulated signals. Camera frames are processed in the browser and are not uploaded by this page. Obtain informed consent for testing; do not use this prototype for grading, hiring, health decisions, or surveillance.


### Live tracking in v0.2
- Shows the live mirrored camera preview with a face-landmark mesh and bounding box.
- Updates total blink events and a rolling last-minute blink count.
- Displays approximate head direction, face position in the frame, eye-open/closed proxy, and movement/stillness.
- These are rough webcam-derived proxies, not clinical or validated attention/emotion measurements. Bright light and a front-facing camera improve tracking.

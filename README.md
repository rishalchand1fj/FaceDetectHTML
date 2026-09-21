# Live Face Detection — Static Browser App

This version runs face detection directly in the visitor's web browser using the webcam and MediaPipe Face Detector.

## Files

- `index.html` — complete application
- `.nojekyll` — tells GitHub Pages to serve the files directly

No Python, Streamlit, Twilio, virtual environment, or server-side CPU is required.

## What the app does

- Uses the visitor's own webcam
- Detects faces live
- Draws green bounding boxes
- Shows face confidence
- Displays the number of detected faces
- Includes Start, Stop, and Full Screen controls
- Runs the detection in the browser

The JavaScript/MediaPipe model is downloaded by the visitor's browser when the page loads. Webcam frames are processed by the page and are not sent to your own Python server.

## Host for free on GitHub Pages

1. Sign in to GitHub.
2. Click **New repository**.
3. Name it something like `live-face-detection`.
4. Choose **Public**.
5. Create the repository.
6. Upload `index.html` and `.nojekyll`.
7. Open **Settings** in the repository.
8. Select **Pages** from the left menu.
9. Under **Build and deployment**, choose:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/(root)**
10. Click **Save**.
11. Wait a few minutes.
12. GitHub will provide a link similar to:

   `https://YOUR-USERNAME.github.io/live-face-detection/`

Open the link, click **Start Camera**, and choose **Allow** when the browser asks for webcam permission.

## Important

Webcam access normally requires HTTPS. GitHub Pages provides HTTPS for `github.io` sites.

If the camera does not start:

- Make sure camera permission is allowed in the browser.
- Close Zoom, Teams, OBS, or another program that may be using the webcam.
- Try Chrome or Edge.
- Refresh the page after changing camera permission.
- Make sure the device has internet access the first time so MediaPipe and its model can load.

## Local testing

Because browsers apply security rules to webcam access, do not rely on opening `index.html` by double-clicking it.

A simple local test from VS Code is to install the **Live Server** extension and choose **Open with Live Server**.

The deployed GitHub Pages version is the recommended test because it runs over HTTPS.

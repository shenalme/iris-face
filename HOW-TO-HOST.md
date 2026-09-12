# Hosting this folder

Everything here is already built. Put these files on any static host that serves
over **HTTPS** - the webcam will not work over plain HTTP.

## Checking which version is deployed

The welcome and completion screens show a **Build** timestamp in small grey
text. If it does not change after you upload, the new files are not live yet.

## Updating an existing GitHub Pages site

Upload `index.html` **and** the whole `assets` folder together - `index.html`
points at hashed filenames inside `assets`, so replacing one without the other
leaves the site stale or broken. Commit, wait for the tick, then hard-refresh
(Ctrl-Shift-R, or Cmd-Shift-R on a Mac). `mediapipe` and `videos` only need
re-uploading if they changed.

## First-time setup

GitHub does not unzip archives. Extract this zip first, then upload what is
inside it.

1. Create a **public** repository.
2. **Add file -> Upload files**, drag in `index.html` and the `assets`,
   `mediapipe` and `videos` folders. Commit.
3. **Settings -> Pages -> Source: Deploy from a branch**, branch `main`,
   folder `/ (root)`. Save.

## What the session looks like now

1. Welcome, camera check.
2. **Screen corners** - four bracket targets in the actual corners, anchoring
   the mapping at the edges.
3. Calibration - nine dots.
4. Validation - five check points.
5. Video, full screen and distraction free.
6. Completion: **Explore results**, plus CSV, detailed CSV and JSON downloads.

The detailed CSV now has 101 columns: gaze and kinematics, fixation and saccade
labels, blink and eye openness, head angles in degrees, estimated viewing
distance in millimetres, brow and mouth measures, and 22 face landmarks.

## Changing the video

Replace `videos/test-video.mp4` with your own MP4 using the same filename, then
redeploy.

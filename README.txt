LUMEN MEDIA PLAYER — MOBILE WEB DEMO
====================================

What it is:
- A standalone, responsive browser prototype for Android Chrome and desktop browsers.
- Lets you select local audio/video files and uses the browser's built-in media playback.
- Includes play/pause, seek, skip 10 seconds, volume, and a session-only recent list.
- Files are not uploaded anywhere.

What it is not:
- This is not a native Android APK.
- It is not a compiled VLC-derived player and does not include VLC's codec engine.
- Browser codec support varies. Try MP4 (H.264/AAC) or MP3 if a file will not play.

How to test on Android:
1. Extract this ZIP using your phone's Files app.
2. Try opening index.html in Chrome. Some Android file managers may open it in a preview rather than Chrome.
3. If local HTML opening is blocked, put index.html on a static hosting service you control, or serve the folder from a computer on the same Wi-Fi and open that local URL on your phone.
4. Tap Choose video or Choose audio and select a media file on your phone.

For local testing from a computer with Python installed, run in this folder:
  python -m http.server 8000
Then open http://COMPUTER-LAN-IP:8000 on the phone, with both devices on the same Wi-Fi.

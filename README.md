# My Story Library — first MVP prototype

This is the first working browser-based MVP shell for the Android-first app. It is designed as an installable Progressive Web App (PWA), which can be added to an Android home screen when hosted over HTTPS.

## Included in this first build
- Warm charcoal / walnut / champagne-gold bookshelf styling.
- Add and organise stories by status and genre.
- Story workspace with chapters and scenes.
- Editable manuscript with local autosave in IndexedDB.
- Basic character profiles and per-story Writing Style Profile.
- Story notes.
- Original source-file storage for PDF and other files.
- Import `.txt`, `.md`, and `.docx` into editable manuscript text. DOCX extraction reads the main document body.
- PDF originals can be stored and opened separately as source documents; PDF text extraction is not implemented yet.
- Export and restore a JSON library backup.
- PWA manifest and service worker shell caching.

## Important limitations
This is an early MVP prototype, not yet the complete production Android app. It does not yet include Gemini API integration, cloud sync, encryption, biometric/PIN lock, PDF text extraction, advanced version history, full Story Bible tabs, or complete DOCX formatting preservation. Local data is stored in the browser profile on the device. Export backups regularly and do not uninstall/clear browser data until you have a backup.

## Run locally for development
Serve this folder from a local web server. For example:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080` in a browser. Service-worker installation requires HTTPS or localhost.

## Install on Android
1. Publish this folder to a secure HTTPS host (for example, a private web host or GitHub Pages repository).
2. Open its HTTPS address in Chrome on Android.
3. Open Chrome's menu and choose **Install app** or **Add to Home screen**.
4. The app opens in its own window. Data is local to that browser installation/profile.

## Importing from NotebookLM
Export notebook notes or generated text to Google Docs where available, then download from Google Docs as `.docx` or `.pdf`. Import DOCX for editable text. Import PDF to retain the original as a source file. For best preservation of chapter structure, export chapters separately and import them into the same story.

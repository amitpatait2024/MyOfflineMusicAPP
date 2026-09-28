# Amify — Offline Music

A private, offline-first music library designed for downloaded songs.

## Features
- Add local audio files from your device.
- Scan a selected Downloads folder on browsers supporting the File System Access API.
- Direct file handles are preferred so the app does not make another copy of the song.
- Fallback browsers can store imported song blobs locally in IndexedDB.
- Create custom albums/playlists (Hindi, Marathi, Haryanvi, Favorites, etc.).
- One song can appear in multiple albums without duplicating the source file.
- Favorites, search, sorting, recently added.
- Offline playback and background-friendly media playback via an HTML audio element.
- Optional original-file deletion where the browser exposes a writable file handle and the user grants permission.
- PWA shell with service worker.

## Important browser limitation
A normal website cannot silently browse another app's Downloads folder. The user must explicitly pick files or a directory. The File System Access API is secure-context-only and has browser/device compatibility limits. See MDN for `showOpenFilePicker()` and `showDirectoryPicker()`.

## Run locally
Serve this folder with any static HTTP server, then open it in a browser:

```bash
python -m http.server 8000
```

Open `http://localhost:8000`.

For installation/offline PWA behavior on a phone, deploy over HTTPS.

# NowYogi

Self-practice yoga app for phone and tablet. A product of Mahboobe Nowruzi Yoga Institute.

- 29 asanas with a 3D animated demonstration, steps, benefits and cautions
- 8 guided programs with a female voice guide, breath cues and timers
- Build, save and share your own cycles
- Health profile that flags poses to take care with
- Progress tracking (saved on the device only)

## Run it

The whole app is one file, `index.html`. Open it in a browser, or host it free with GitHub Pages:

1. Create a repository and upload these files.
2. Go to Settings → Pages, choose "Deploy from a branch", branch `main`, folder `/ (root)`, and save.
3. The app is live at `https://<your-username>.github.io/<repository-name>/` after a minute or two.

An internet connection is needed on first load for the fonts and the 3D library (three.js 0.149.0 from jsDelivr). Without 3D support the app falls back to a flat character.

## Adding real videos and recorded voice

Put clips in `videos/` and recordings in `audio/`, named with the pose ID (for example `down-dog.mp4`), then list them in the `MEDIA` map near the top of the script in `index.html`:

```js
const MEDIA = {
  "down-dog": { video: "videos/down-dog.mp4", audio: "audio/down-dog.mp3" }
};
```

Film the right side only; the left side is mirrored automatically.

## Icons and "Add to Home Screen"

`icons/` holds the lotus logo as PNG files and `manifest.json` describes the app, so students can add NowYogi to their home screen and open it full-screen like an installed app:

- iPhone / iPad (Safari): Share → Add to Home Screen
- Android (Chrome): menu → Add to Home screen / Install app

`icons/logo-1024.png` is a large transparent logo for print or social media.

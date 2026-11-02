# NoteWing Free — Guitar Practice Studio

A free, original, browser-based guitar learning and improvisation app. It is designed to deploy to **GitHub Pages** with no build step, paid API, subscription, or backend required.

## Features

- Dashboard with XP, practice streak, time, lesson completion and activity history.
- Five original learning units: licks, chord tones, approach notes, enclosures and building an eight-bar solo.
- Original backing progressions generated locally with the Web Audio API.
- Eight-bar solo builder with note grid, playback, starter patterns and local draft saving.
- Interactive six-string fretboard with major, natural minor, pentatonic, blues and Dorian scales.
- Chromatic microphone tuner using browser audio input and autocorrelation pitch detection.
- Chord library with common chord qualities, note tones, voicing diagrams and generated playback.
- Interval ear-training exercises.
- Metronome with tempo presets and time signatures.
- Local profile, achievements, practice history and JSON export.

## Run locally

You can simply open `index.html` in a modern browser. Most features work from a local file. Microphone access for the tuner and listening challenge normally requires a secure context, so use localhost:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy to GitHub Pages

1. Create a new GitHub repository, for example `notewing-free`.
2. Upload `index.html`, `styles.css`, `app.js`, and this README to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. Your site will be available at `https://YOUR-USERNAME.github.io/notewing-free/`.

No package installation, build command, environment variables, or paid API key is required.

## Data and privacy

- Practice progress, profile, completed units and saved solo drafts are stored in the browser's local storage on the device.
- Use **Profile → Export data** to download a JSON backup.
- Microphone features request access only when you start them. Audio is processed in the browser and is not uploaded by this app.
- Clearing browser site data or using a different browser/device will not carry local progress across. Export your data first if you want a backup.
- Google Fonts is used for typography; the rest of the app is self-contained. You can remove the `@import` line in `styles.css` to avoid that external request.

## Notes and limitations

This project uses original lesson phrases and generated backing harmony rather than reproducing proprietary NoteWing content. The backing tracks are simple synthesised chord pads, not studio-recorded guitar/band tracks. The microphone pitch detector is a lightweight educational tuner; noisy rooms, low-quality microphones, harmonics, and chords can affect accuracy. Tune one string at a time in a quiet environment.

The performance challenge estimates whether detected notes are chord tones during a simple timed progression. It is a learning aid, not professional-grade transcription or a definitive performance assessment. The solo builder is a note-grid sketchpad; it does not yet export MIDI or standard notation.

## Customisation

- Edit `UNITS` in `app.js` to add original lessons.
- Edit `PROGRESSIONS` to add original backing progressions.
- Edit `SCALE` to add scale formulas.
- Edit `VOICINGS` to add chord fingerings.
- Adjust colours and layout tokens at the top of `styles.css`.

## Licence

MIT. See `LICENSE`.

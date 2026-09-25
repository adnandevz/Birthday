# Mission [Her Name]

A static, mobile-first cinematic birthday experience for GitHub Pages. It uses only HTML, CSS, and browser JavaScript. Missing photos, audio, microphone access, local storage, sharing, and canvas export all have graceful fallbacks.

## Edit the personal content

1. Open `js/config.js` and edit `herName`, `nickname`, `birthday`, `finalMessage`, audio paths, photos, and secret messages.
2. Edit the short notes on screen 2 in `content/notes.js`.
3. Edit memories and descriptions in `content/memories.js`.
4. Edit balloon captions and notes in `content/messages.js`.
5. Edit the long heartfelt letter in `content/letter.js`. Add as many paragraphs as you like to the `birthdayLetter` array.
6. Edit the final Secret Room and Birthday Time Capsule wording in `js/config.js` under `secretRoom` and `capsule`.

Place photos in `assets/photos/` and update the relative paths in `js/config.js`, `content/messages.js`, or `content/memories.js`. The first photo in `config.photos` appears on the opening screen. Missing images have graceful fallbacks. Put `letter.mp3` in `assets/music/` to play music while the letter is being read.

The final **Keep this memory** button creates a bright downloadable/shareable birthday card using the name, birthday date, and final message from `js/config.js`.

## Run locally

Opening `index.html` directly works for most scenes. Microphone permissions require a secure context, so use a local server when testing candles:

```powershell
python -m http.server 8080
```

Open `http://localhost:8080/`. On a phone, deploy to GitHub Pages or use an HTTPS local tunnel. Tap **Enable microphone**, grant permission, and blow firmly for a short moment. The microphone is analyzed locally and tracks stop immediately after detection; nothing is recorded or uploaded.

## Deploy to GitHub Pages

1. Create a new GitHub repository.
2. Upload or push the contents of this folder to the repository's default branch.
3. In **Settings > Pages**, choose **Deploy from a branch**, select the default branch and `/ (root)`, then save.
4. Open the generated HTTPS URL, usually `https://username.github.io/repository-name/`.
5. Replace all bracketed placeholders before sharing.

## QR code

Open `qr.html`, paste the final deployed HTTPS URL, and choose **Generate QR**. Save or share the resulting image. No destination is embedded in the project.

## Progress and testing

Progress, discovered memories, balloons, and cake selections are stored in local storage. Use `index.html?dev=true` for the developer panel, including scene jumps and reset. To reset normally, clear site data for the page in browser settings. Test at 320, 360, 375, 390, 412, and 430px widths plus tablet and desktop. The CSS includes safe-area padding, no absolute asset paths, reduced-motion support, large touch targets, and a microphone fallback button.

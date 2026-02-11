# How to host Pier Pressure and add it to your phone

Your game is set up as a **Progressive Web App (PWA)**. Once it’s on a website, you can add it to your phone’s home screen and it will open like an app. Progress is saved in the browser (per device).

---

## Step 1: Put the game on a website (hosting)

You need to upload your project so it’s served over **HTTPS**. Here are simple options.

### Option A: GitHub Pages (free, good if you use GitHub)

1. Create a repo on [GitHub](https://github.com) (e.g. `PierPressure`).
2. Upload your project folder so the repo contains:
   - `index.html`
   - `manifest.json`
   - `icon.svg`
   - `sw.js`
   (All at the **root** of the repo, not inside a subfolder.)
3. In the repo: **Settings → Pages**.
4. Under **Source**, choose **Deploy from a branch**.
5. Branch: **main** (or **master**), folder: **/ (root)**. Save.
6. After a minute or two, your game will be at:
   - **https://YOUR_USERNAME.github.io/PierPressure/**  
   (Replace `YOUR_USERNAME` and `PierPressure` with your GitHub username and repo name.)

### Option B: Netlify (free, no GitHub needed)

1. Go to [netlify.com](https://www.netlify.com) and sign up (free).
2. Drag and drop your **PierPressure folder** (the one with `index.html`, `manifest.json`, `icon.svg`, `sw.js`) onto the Netlify “Deploy” area.
3. Netlify will give you a URL like `https://something-random.netlify.app`. You can rename it in **Domain settings** (e.g. `pier-pressure.netlify.app`).

### Option C: Other hosts

You can use any static host (Vercel, Cloudflare Pages, etc.) the same way: upload the same files so `index.html` is the main page and the URLs for `manifest.json`, `icon.svg`, and `sw.js` work.

---

## Step 2: Add to your phone’s home screen

After the game is live at an HTTPS URL:

### On iPhone (Safari)

1. Open the game’s URL in **Safari** (e.g. `https://YOUR_USERNAME.github.io/PierPressure/`).
2. Tap the **Share** button (square with arrow).
3. Scroll and tap **Add to Home Screen**.
4. Edit the name if you want (e.g. “Pier Pressure”), then tap **Add**.

An icon will appear on your home screen. Tapping it opens the game in full screen like an app. Your save data stays in Safari on that device.

### On Android (Chrome)

1. Open the game’s URL in **Chrome**.
2. Tap the **menu** (three dots) → **Add to Home screen** or **Install app**.
3. Confirm the name and tap **Add** or **Install**.

The game will appear on your home screen and can open in its own window. Saves are kept in Chrome on that device.

---

## Notes

- **Saves**: The game uses the browser’s storage (localStorage). Each device/browser has its own save. Clearing site data for the URL will clear the save on that device.
- **Offline**: After you’ve opened the game at least once, the service worker can let it run offline on that device (depending on the browser).
- **Icon**: The app uses `icon.svg` for the home screen icon. If you want a different image, replace `icon.svg` with a square image (e.g. 512×512 PNG) and update `manifest.json` to point to it.

That’s it. Once the site is live, use “Add to Home Screen” and you’ll have Pier Pressure as a saveable app on your phone.

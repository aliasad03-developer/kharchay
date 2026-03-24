# Kharchay – Personal Finance PWA

> Track expenses, income, savings, investments, budgets and more. Works fully offline.

---

## 📁 Files in this folder

| File | Purpose |
|------|---------|
| `index.html` | The entire app (single file) |
| `sw.js` | Service Worker – enables offline use |
| `manifest.json` | PWA manifest – makes it installable |
| `icon-192.png` | App icon (Android home screen) |
| `icon-512.png` | App icon (splash screen / PWABuilder) |
| `apple-touch-icon.png` | App icon (iPhone home screen) |
| `favicon-32.png` | Browser tab icon |

---

## 🚀 Step 1 — Deploy to GitHub Pages (free hosting)

1. Go to **github.com** → **New repository**
2. Name it `kharchay` (or anything you like)
3. Set visibility to **Public**
4. Click **Create repository**
5. Upload ALL files from this folder:
   - Click **uploading an existing file**
   - Drag all 7 files in → **Commit changes**
6. Go to **Settings → Pages**
7. Under **Source**, select `Deploy from a branch` → `main` → `/ (root)` → **Save**
8. Wait ~60 seconds, your app will be live at:
   ```
   https://YOUR-USERNAME.github.io/kharchay/
   ```

---

## 📱 Step 2 — Install as PWA on your phone (no APK needed!)

### iPhone (Safari)
1. Open your GitHub Pages URL in **Safari**
2. Tap the **Share** button (box with arrow)
3. Tap **Add to Home Screen**
4. Tap **Add** → Done! App icon appears on your home screen

### Android (Chrome)
1. Open your GitHub Pages URL in **Chrome**
2. Chrome will show a banner: **"Add Kharchay to Home Screen"** — tap it
3. Or tap the **3-dot menu → Add to Home Screen**
4. Tap **Install** → Done!

> The app works **100% offline** after first load. All data is saved on your device.

---

## 📦 Step 3 — Convert to APK (optional, for Google Play or direct install)

Use **PWABuilder** (free, by Microsoft):

1. Go to **pwabuilder.com**
2. Enter your GitHub Pages URL
3. Click **Start** → it will analyse your PWA
4. Click **Package for stores** → choose **Android**
5. Click **Download** to get the `.apk` or `.aab` file
6. Install the APK directly on Android:
   - Transfer to phone → tap file → **Install** (enable "Unknown sources" if prompted)
7. Or upload `.aab` to **Google Play Console** to publish on the Play Store

### Alternative: Bubblewrap (advanced)
```bash
npm install -g @bubblewrap/cli
bubblewrap init --manifest https://YOUR-USERNAME.github.io/kharchay/manifest.json
bubblewrap build
```

---

## 🔒 Data & Privacy

- All data is stored **locally on your device** using `localStorage`
- Nothing is sent to any server
- Clearing browser data / app data will erase your records
- **Export to Excel regularly** from the app as a backup

---

## 🛠 Local development

Just open `index.html` in any browser. No build tools needed.

For proper service worker testing, serve locally:
```bash
npx serve .
# or
python3 -m http.server 8080
```
Then open `http://localhost:8080`

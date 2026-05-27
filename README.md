# 🎲 Party Quest

**Find your adventuring party. Swipe. Match. Roll dice together.**

Live app: https://ariqureshi73.github.io/party-quest/

---

## 🚀 Play Store Submission Guide

### Step 1 — Prerequisites
- Install [Node.js](https://nodejs.org/) (v16+)
- Install [Android Studio](https://developer.android.com/studio) (for the Android SDK)
- Create a [Google Play Developer account](https://play.google.com/console/) ($25 one-time fee)

### Step 2 — Install Bubblewrap (Google's official TWA tool)
```bash
npm install -g @bubblewrap/cli
```

### Step 3 — Build the APK
```bash
git clone https://github.com/ariqureshi73/party-quest.git
cd party-quest
bubblewrap init --manifest https://ariqureshi73.github.io/party-quest/manifest.json
bubblewrap build
```
This generates `app-release-signed.apk` and `app-release.aab` (AAB is required for Play Store).

### Step 4 — Digital Asset Links (REQUIRED)
Google Play requires you to verify domain ownership. Add this file to your repo:

`.well-known/assetlinks.json` — generated automatically by Bubblewrap after you create your keystore.

### Step 5 — Submit to Play Store
1. Go to [Google Play Console](https://play.google.com/console/)
2. Create new app → "Party Quest"
3. Upload the `.aab` file under **Release > Production**
4. Fill in store listing: description, screenshots, category (Games > Role Playing)
5. Set content rating (Everyone)
6. Submit for review (~3-7 days)

---

## 🔄 Auto-Deploy
Every update to `index.html` on the `main` branch automatically deploys to GitHub Pages within ~30 seconds.

## 📜 Version History
All changes tracked via Git commits. View history:
https://github.com/ariqureshi73/party-quest/commits/main

---

## Tech Stack
- Vanilla JS / HTML5 / CSS3
- Base44 backend API (entities, auth)
- GitHub Pages hosting
- PWA (installable on iOS & Android)
- Stripe (DM Tier subscriptions)

# 3rd Ear 🐾
### Dog Training Session Recorder · by iSpeakDog / The Dog Director

---

## What It Does

**3rd Ear** is a Progressive Web App (PWA) that:
- Records your voice during dog training sessions using your iPhone's built-in microphone
- Transcribes speech in real-time (no internet needed for transcription)
- Sends the transcript to Claude AI to automatically generate a structured wiki entry
- Saves all sessions locally on your phone — they persist between visits
- Exports sessions to Google Drive as formatted text files

---

## How to Get It On Your iPhone (Free, ~2 Minutes)

### Option 1: GitHub Pages (Recommended — Free & Permanent)

1. **Go to [github.com](https://github.com)** and sign in (or create a free account)
2. Click the **+** button in the top right → **New repository**
3. Name it `3rd-ear` — set it to **Public** — click **Create repository**
4. Click **uploading an existing file** (link on the empty repo page)
5. **Drag all 5 files** into the upload area:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `icon-192.png`
   - `icon-512.png`
6. Click **Commit changes**
7. Go to **Settings** → **Pages** (in left sidebar)
8. Under "Source", select **Deploy from a branch** → Branch: **main** → folder: **/ (root)** → **Save**
9. Wait ~60 seconds, then your app is live at:
   `https://YOUR-GITHUB-USERNAME.github.io/3rd-ear/`

### Add to iPhone Home Screen:
1. Open that URL in **Safari** (must be Safari, not Chrome)
2. Tap the **Share** button (box with arrow pointing up)
3. Scroll down → tap **"Add to Home Screen"**
4. Tap **Add**
5. 3rd Ear now appears on your home screen like a real app! 🎉

---

### Option 2: Netlify Drop (Even Easier — 30 Seconds)

1. Go to **[app.netlify.com/drop](https://app.netlify.com/drop)**
2. Drag your entire `3rdear-pwa` folder onto the page
3. Done — you get an instant URL like `https://random-name-123.netlify.app`
4. Follow the "Add to Home Screen" steps above with that URL

---

## First-Time Setup (In the App)

1. Open the app → tap **Settings** (⚙️)
2. Enter your **dog's name** and **your name**
3. Add your **training goals** (e.g., "Off-leash recall, loose leash walking")
4. Paste your **Claude API Key** (get one free at [console.anthropic.com](https://console.anthropic.com))
5. Optionally add a **Google Drive token** to enable export
6. Tap **Save Settings**

---

## Using the App

### Recording a Session
1. Tap the **Record** tab (🎙️)
2. Tap the **big blue mic button** — it turns red when recording
3. Speak naturally about what you're doing during training
4. Tap the **stop button** (⏹) when done
5. Wait a few seconds — Claude will generate your wiki entry
6. Tap **View Entry** to read the AI-generated notes

### Viewing Your Wiki
- Tap the **Wiki** tab (📖) to see all sessions
- Tap any session to view the full wiki entry and transcript
- Toggle between **Wiki Entry** and **Transcript** views
- Tap **Export to Google Drive** to save a copy to your Drive

---

## Getting a Google Drive Access Token

Google Drive tokens expire every ~1 hour, so you'll get a fresh one when you want to export:

1. Go to [developers.google.com/oauthplayground](https://developers.google.com/oauthplayground)
2. In the left panel, find **Drive API v3**
3. Select `https://www.googleapis.com/auth/drive.file`
4. Click **Authorize APIs** → sign in with your Google account
5. Click **Exchange authorization code for tokens**
6. Copy the **Access token** value
7. Paste it into **Settings → Google Drive Access Token** in 3rd Ear

---

## Getting a Claude API Key

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up / log in
3. Go to **API Keys** → **Create Key**
4. Copy the key (starts with `sk-ant-...`)
5. Paste into **Settings → Claude API Key** in 3rd Ear

> **Cost note:** Claude API calls are very affordable. A typical training session wiki entry costs less than $0.01.

---

## Tips for Best Transcription

- **Use Safari on iPhone** — it has the best speech recognition support
- Speak clearly and at a moderate pace
- Minimize background noise (wind, barking, etc.)
- Say dog and command names clearly
- The transcription works offline — Claude wiki generation requires internet

---

## Privacy

- **Everything stays on your phone** — sessions are stored in your browser's local storage
- Transcripts are sent to Anthropic's Claude API only when generating wiki entries
- Nothing is ever uploaded to any server unless you explicitly export to Drive
- Your API keys are stored only in your browser's localStorage

---

## File Structure

```
3rdear-pwa/
├── index.html         Main app (all JS + CSS inline)
├── manifest.json      PWA manifest for "Add to Home Screen"
├── service-worker.js  Offline support
├── icon-192.png       App icon
└── icon-512.png       App icon (large)
```

---

*Built for Tommy Stark · iSpeakDog / The Dog Director · Orange County, CA*

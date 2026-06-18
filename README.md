# Meeting Notes PWA

A Progressive Web App that records meetings, transcribes speech in real time, and uses Claude AI to generate a summary and action items.

## Files

```
meeting-notes-pwa/
├── index.html       ← The entire app
├── manifest.json    ← PWA install config
├── sw.js            ← Service worker (offline support)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Deploy to GitHub Pages (free, ~5 minutes)

1. Go to [github.com](https://github.com) and sign in (or create a free account)
2. Click **New repository** → name it `meeting-notes` → set to **Public** → click **Create repository**
3. Click **Add file → Upload files** and drag in all four files/folders above
4. Click **Commit changes**
5. Go to **Settings → Pages → Source → Deploy from branch → main / root** → Save
6. Your app will be live at `https://YOUR-USERNAME.github.io/meeting-notes` within ~2 minutes

## Add to your phone's home screen

**iPhone (Safari):**
1. Open the URL above in Safari
2. Tap the Share button (square with arrow)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add** — it now appears as an app icon

**Android (Chrome):**
1. Open the URL in Chrome
2. Tap the three-dot menu
3. Tap **Add to Home screen** or look for the install banner

**Desktop (Chrome / Edge):**
- Look for the install icon in the address bar, or go to the three-dot menu → **Install app**

## First-time setup

When you open the app, it will immediately ask for your **Anthropic API key**.

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign in → click **API Keys** → **Create Key**
3. Copy the key (starts with `sk-ant-`)
4. Paste it into the app's Settings drawer and tap **Save**

Your key is stored only on your device in `localStorage` and is never sent anywhere except Anthropic's API.

## How to use

1. Tap the **microphone button** to start recording
2. Speak — the transcript appears in real time
3. Tap the button again to **stop**
4. Tap **Analyze meeting** to generate a summary and action items
5. Use the **Copy** buttons to grab results for email, OneNote, etc.
6. Tap the **↑ New meeting** icon (top left) to clear and start fresh

## Notes

- Speech recognition requires Chrome or Edge (iOS Safari works too but may be less accurate)
- The app works offline once loaded — only the Analyze step needs internet
- Microphone permission is required and requested on first use

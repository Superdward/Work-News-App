# Product Intelligence · Weekly Digest PWA

A personal news digest app for product owners in digital account opening and SME banking.

## Files

```
index.html      ← Main app (everything is in here)
manifest.json   ← PWA metadata (name, icon, colours)
sw.js           ← Service worker (offline shell caching)
icon-192.svg    ← App icon (home screen, small)
icon-512.svg    ← App icon (splash screen, large)
```

---

## Installing on Android

1. Open the URL in **Chrome**
2. Tap the **⋮ menu → Add to Home screen**
3. Or wait 2 seconds — an install banner will appear automatically
4. Tap **Install** → it appears on your home screen like a native app

## Installing on iPhone

1. Open the URL in **Safari** (must be Safari for PWA install on iOS)
2. Tap the **Share button → Add to Home Screen**
3. Tap **Add**

---

## How it works

- Tap the topics you want (or select all)
- Hit **Generate digest**
- The app searches the web in real time via the Anthropic API
- Each topic takes ~15 seconds; results appear after all topics finish
- The app shell works offline (you'll need internet to generate new digests)

---

## Customising

All topics and search queries are in the `CATEGORIES` array near the top of `index.html`.
The AI briefing style is in `SYSTEM_PROMPT` — edit it to change tone, structure, or focus.

---

## Notes

- The Anthropic API key is handled by Claude.ai infrastructure — no key needed in the file
- Last digest date is remembered between sessions via localStorage
- Install prompt is only shown once (dismissed state is saved)

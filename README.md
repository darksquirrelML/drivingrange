# 🏌️ Driving Range

A 3D golf driving range trainer built as a Progressive Web App (PWA). Swing your phone like a real golf club — the app detects your actual swing motion using the phone's motion sensors.

🎮 **[Play Now](https://darksquirrelml.github.io/drivingrange/)**

---

## How to Play

### Hold your phone
Hold your phone upright (portrait), face forward — like gripping a golf club handle.

### The Swing (3 phases)
1. **Backswing** — raise phone up. The ring turns gold when backswing is detected.
2. **At the top** — brief pause at the top of your swing.
3. **Downswing** — swing down fast. Speed = power. The faster you swing, the further the ball goes.

### Straightness
At the moment of impact, the tilt angle of your phone (gamma) determines direction:
- Phone tilted left → ball goes left
- Phone straight → ball goes straight
- Phone tilted right → ball goes right

Just like a real golf club face angle at impact!

---

## Game Modes

| Mode | Goal |
|------|------|
| 💪 **Power Mode** | Swing as hard as you can — how far can you drive? |
| 🎯 **Straightness Mode** | Fixed power — keep the ball on the fairway. Accuracy is your score. |

---

## Scoring

### Power Mode
| Distance | Points |
|----------|--------|
| 50m ring  | 5 pts  |
| 100m ring | 10 pts |
| 150m ring | 20 pts |
| 200m ring | 35 pts |
| 250m ring | 50 pts |

### Straightness Mode
Score is based on accuracy percentage — how close to straight your shot was. Bullseye (within 5°) earns a bonus 20 pts.

---

## Session
- **5 shots** per session
- Results card shows: best drive, average distance, best accuracy, total score
- Each shot rated: Monster Drive 🔥 / Great Drive 💪 / Bullseye 🎯 / etc.

---

## Tech Stack

- **Three.js** — 3D rendering (fairway, distance rings, trees, ball flight)
- **DeviceMotion API** — real swing detection (backswing → downswing phases)
- **DeviceOrientation API** — gamma angle at impact for direction
- **Web Audio API** — all sounds generated in code (no audio files)
- **PWA** — installable on Android home screen, works offline
- Pure **HTML + CSS + JavaScript** — no frameworks, no build tools
- Hosted on **GitHub Pages**

---

## Install as App (Android)

1. Open the link in **Chrome**
2. Tap ⋮ menu → **Add to Home screen**
3. Play from your home screen like a native app

---

## Files

```
drivingrange/
├── index.html       ← entire game
├── manifest.json    ← PWA config
├── sw.js            ← service worker (offline support)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

---

## Tips for Best Results

- Swing in a **clear open space** — you need room for a full golf swing motion
- Hold phone **firmly** — don't let it slip at impact
- In **Straightness Mode** — focus on keeping your wrist straight through impact
- The tap fallback button at the bottom works for desktop testing without motion sensors

---

Made with ⛳ — no frameworks, no build tools, just one HTML file.

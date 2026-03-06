# 🌴 Cardano Quest Island — Setup Guide

## One-time setup (5 minutes)

### Step 1 — Install Node.js
If you don't have Node.js installed:
👉 Download from https://nodejs.org (choose the LTS version)

### Step 2 — Open the project in VS Code
1. Unzip this folder anywhere you like (e.g. Desktop)
2. Open VS Code
3. Go to **File → Open Folder** and select the `cardano-quest` folder

### Step 3 — Open the Terminal in VS Code
- Press **Ctrl + `** (backtick) OR go to **Terminal → New Terminal**

### Step 4 — Install dependencies
In the terminal, type:
```
npm install
```
Wait for it to finish (30–60 seconds the first time).

### Step 5 — Start the game!
```
npm run dev
```

Then open your browser and go to:
👉 **http://localhost:5173**

---

## Project file structure

```
cardano-quest/
├── index.html          ← Entry point HTML
├── package.json        ← Project config & dependencies
├── vite.config.js      ← Build tool config
└── src/
    ├── main.jsx        ← React entry point
    ├── App.jsx         ← Main game logic & UI panels
    ├── Scene.jsx       ← All 3D objects (island, player, stations)
    ├── data.js         ← Station content, questions, tokens
    └── styles.css      ← All UI styles
```

## To edit game content
- **Add/edit questions:** Open `src/data.js` → find the station → edit the `questions` array
- **Add/edit lessons:** Open `src/data.js` → find the station → edit the `lessons` array
- **Add a new station:** Add a new object to the `STATIONS` array in `src/data.js`

## To build for your website
```
npm run build
```
This creates a `dist/` folder you can upload to any web host (Netlify, Vercel, GitHub Pages, etc.)

---

## Controls
| Key | Action |
|-----|--------|
| WASD or Arrow Keys | Move |
| Shift | Sprint |
| E (or click platform) | Enter station |

---

## Phase 3 roadmap
- [ ] Supabase backend for global leaderboard
- [ ] Cardano wallet connect (Mesh.js)
- [ ] Sound effects & ambient music
- [ ] Mobile joystick support
- [ ] Testnet NFT badges on completion

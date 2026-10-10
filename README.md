# 🌿 FloraQuest (TouchGrass AI)

> **Hacktoberfest Open-Source AI Challenge: Week 1 — Touch Grass**  
> An open-weight AI companion engineered to get people off their screens and into nature in **under 60 seconds**.

![License: MIT](https://img.shields.io/badge/License-MIT-emerald)
![Inference: 100% Local](https://img.shields.io/badge/Inference-Local%20%2F%20Offline-blue)
![Models: Open--Weight](https://img.shields.io/badge/Model-MobileNet--v2%20OpenWeights-amber)

---

## 🍃 Core Philosophy

Most apps keep you staring at screens. **FloraQuest** is built on the opposite premise:
- **Screen time limit: < 60 seconds.** Get your answer, pocket your phone, and look up at the trees.
- **100% Offline-Ready:** Zero cloud calls. Zero API keys. Uses open-weight neural vision running in WebAssembly. Works deep on trails with no cellular signal.

---

## ✨ Features

1. **🍂 Offline Trail Specimen ID:**
   - Drop or photograph leaves, fungi, bark, and birds.
   - Runs client-side neural classification via Hugging Face `@xenova/transformers` (`MobileNet-v2`).
   - Gives an instant 1-sentence field guide fact + an "Eyes-Up Trail Challenge" prompt to look away from your screen.

2. **🍁 Fall Foliage & Run Club Scout:**
   - Configure your available time (15–90 min), activity (Run, Hike, Bike), and target terrain (Fall Foliage, River Creek, Evergreen Pine, Meadow).
   - Generates route waypoints and an eyes-up 3-item sensory scavenger hunt.
   - Includes a printable "Pocket Trail Card" option.

3. **🌱 Autumn Frost & Soil Garden Radar:**
   - Select your climate hardiness zone (Zones 4–9).
   - Gives estimated frost countdown and actionable outdoor garden tasks: What to direct-sow (garlic, winter greens, bulbs), harvest before hard freeze, and soil mulching steps.

4. **🌲 Screen-Off Zen Companion:**
   - Ambient screen-dimming mode that tracks outdoor minutes and deep breaths.
   - Includes a **procedural Web Audio synthesizer** that generates soothing canopy breeze and birdsong completely in code without downloading audio files.

---

## 🚀 Quick Start (Running Locally)

### Option 1: Direct Browser Launch
Simply double-click `index.html` in your file explorer or open it in Google Chrome, Microsoft Edge, Firefox, or Safari!

### Option 2: Local Static Server (Recommended)
You can run any lightweight local server:

**Using Python:**
```bash
cd touchgrass-ai
python -m http.server 3000
```
Then visit `http://localhost:3000`.

**Using Node.js:**
```bash
npx serve .
```

---

## 📦 Project Structure

```
FloraQuest-AI/
├── index.html          # Semantic HTML5 layout with tabs & modal
├── style.css           # Custom obsidian nature design system
├── app.js              # Client-side Transformers.js AI inference & Web Audio
├── PROJECT_DETAILS.md  # Detailed technical specifications & architecture
└── README.md           # Quickstart and overview
```

---

## 🔓 Why Open Innovation Matters
- **Trail Independence:** No cell towers needed in remote nature reserves.
- **Privacy:** No GPS or camera data sent to external cloud servers.
- **Free for Everyone:** Zero token costs or API subscriptions.

---

## 📜 License
MIT License — Free to use, adapt, and share for outdoor enthusiasts everywhere.

*This is a submission for the [Hacktoberfest Open-Source AI Challenge Week 1: Touch Grass](https://dev.to/challenges/hacktoberfest-week1-2026-10-05)*

## What I Built

**FloraQuest (TouchGrass AI)** is an offline-first nature scout powered by open-weight AI models, designed specifically to get people off their screens and into the outdoors in **under 60 seconds**.

### The Problem
Most modern outdoors and hiking apps paradoxically trap people on screens: endlessly scrolling feeds, checking notifications, and tracking metrics while standing underneath vibrant forest canopies.

### The Solution: The "Rule of < 60 Seconds"
FloraQuest inverts the digital experience. It is strictly engineered so that the screen is the shortest part of your day:
1. **Offline Trail Specimen Classifier:** Identifies leaves, mushrooms, bark, and birds on the trail in milliseconds using open-weight vision models (`MobileNet-v2`) running directly inside browser WebAssembly. Zero cell signal required!
2. **Fall Foliage & Run Club Scout:** Pick your available time (15–90 min) and outdoor terrain (Fall Foliage, River Creek, Evergreen Pine, Golden Meadow) to generate a trail itinerary and an "eyes-up" 3-item sensory scavenger hunt (e.g., finding acorn caps, listening for rushing water).
3. **Autumn Frost & Soil Garden Radar:** Tells you what to direct-sow (garlic, winter spinach, bulbs), harvest, or mulch this week based on regional frost dates, encouraging users to get their hands in real dirt.
4. **Screen-Off Zen Walk:** Features a procedural Web Audio forest breeze and birdsong synthesizer that dims the screen, tracks outdoor walking minutes, and tells you to put your phone in your pocket.

---

## Demo

- **Live Local Demo:** Simply double-click `index.html` or run `npx serve .` in the project directory!
- **Zero API Keys or Cloud Setup:** Works out of the box with zero external configuration.
- **Offline Capable:** Cached completely in browser storage via Transformers.js WebAssembly.

---

## Code

The full source code is hosted open-source:
- **Repository:** https://github.com/SrujanTag/FloraQuest-AI
- **Stack:** Pure HTML5, Modern Vanilla CSS (Custom Design System with Glassmorphic Obsidian Aesthetics), Vanilla JavaScript (ES Modules), Hugging Face `@xenova/transformers`, Web Audio API, WebAssembly.

---

## How I Built It

FloraQuest is architected from the ground up around **open-source AI and client-side inference**:

1. **Open-Weight Vision Pipeline:** We integrated Hugging Face's `@xenova/transformers` library to run `Xenova/mobilenet_v2_1.0_224` directly on-device in WebAssembly.
2. **Local Model Caching:** The open weights (~8MB) are cached locally in the browser's `CacheStorage`. Once loaded once, you can disconnect Wi-Fi and cell signal entirely and take your device onto any backcountry trail.
3. **Offline Specimen Heuristic Engine:** For immediate offline zero-network first runs, a built-in botanical trail database provides field guide facts and outdoor observation challenges with zero server dependencies.
4. **Procedural Web Audio Synthesizer:** Instead of downloading bulky audio files, the Screen-Off companion generates ambient canopy breeze and gentle birdsong procedurally using pink-noise bandpass filters and sine wave frequency modulations.

---

## Why Does Open Innovation Matter?

Open innovation is not just a feature of FloraQuest; **it is the single reason the application can function outdoors**:

- **Trail Independence (Zero Connectivity):** Closed APIs (such as OpenAI, Gemini, or Claude) are useless the moment you hike into a valley, canyon, or national park with no cell signal. Open-weight models run on the local CPU/GPU in your pocket, ensuring reliability anywhere on Earth.
- **Data Privacy on the Trail:** Closed APIs require sending your camera photos and potentially embedded GPS metadata to corporate servers. Open-weight local inference processes pixels strictly in memory on your device—zero telemetry, zero server logs.
- **Zero Cost Forever ($0 API Bills):** Commercial APIs charge per token and image, creating recurring bills for open-source community projects. Open weights cost $0 to run indefinitely, making nature tools accessible to community gardening clubs, schools, and hikers without paywalls.
- **Hackability and Model Swapping:** Because the architecture is open-source, any developer can swap the classification pipeline to higher-parameter Vision Transformers (`ViT`), fine-tune it on native flora of their home region, or connect to a local Ollama instance without asking for permission.

---

## My Agent Session

Built with the assistance of Antigravity AI pair programming agent, organizing the offline WebAssembly model loading, sensory scavenger hunt generator, and obsidian nature design system.

---

## Prize Categories

- **Hacktoberfest Open-Source AI Challenge Week 1: Touch Grass**

# 🌿 FloraQuest-AI: Technical Architecture & Project Details

> Detailed technical specifications, architecture decisions, and offline-first open-weight model integration for FloraQuest.

---

## 1. Project Overview

FloraQuest is an open-source, client-side web application designed to encourage people to disconnect from screens and explore the outdoors in under 60 seconds.

### Core Modules
- **Trail Specimen Classifier**: Image classification of botanical and trail specimens (leaves, fungi, trees, birds) using open-weight neural networks.
- **Fall Foliage & Run Club Scout**: Custom route builder with a 3-item sensory scavenger hunt for autumn nature walks and trail runs.
- **Frost & Soil Radar**: Planting and harvesting tracker based on climate hardiness zones and local first-frost dates.
- **Screen-Off Zen Companion**: Procedural ambient sound generator using the Web Audio API with minimal screen usage.

---

## 2. Technical Architecture

```
+-------------------------------------------------------------+
|                        Browser Client                       |
|                                                             |
|  +--------------------+             +--------------------+  |
|  |     HTML5 / CSS3   |             |   Web Audio API    |  |
|  | Modern Obsidian UI |             | Forest Synthesizer |  |
|  +---------+----------+             +---------+----------+  |
|            |                                  |             |
|  +---------v----------------------------------v----------+  |
|  |                      app.js Core                      |  |
|  |         State Management & Route Generator            |  |
|  +---------+----------------------------------+----------+  |
|            |                                  |             |
|  +---------v----------+             +---------v----------+  |
|  | Transformers.js    |             | Local Heuristic    |  |
|  | WebAssembly ONNX   |             | Fallback Engine    |  |
|  | (MobileNet-v2)     |             | (Trail Database)   |  |
|  +--------------------+             +--------------------+  |
+-------------------------------------------------------------+
```

### Key Technologies
- **Frontend Core**: Vanilla HTML5 and ES6+ JavaScript modules.
- **Design System**: Vanilla CSS3 with CSS custom properties, glassmorphism, responsive grid layout, and zero third-party UI framework overhead.
- **AI Inference Engine**: Hugging Face `@xenova/transformers` running the `MobileNet-v2` (`Xenova/mobilenet_v2_1.0_224`) open-weight vision model in WebAssembly via ONNX Runtime Web.
- **Audio Synthesis**: Procedural pink noise generator with bandpass modulation and sine oscillator chirps built with the Web Audio API.

---

## 3. Open Innovation & Model Independence

- **Zero Cloud Dependence**: All inference runs locally in client memory. No network requests are made during inference.
- **Privacy Preservation**: User photos and location data never leave the client device.
- **Zero Operating Costs**: Free to host and run indefinitely with $0 API overhead.
- **Model Modularity**: The inference pipeline can be switched to other open architectures (such as ViT or fine-tuned regional checkpoints) by updating the model identifier.

---

## 4. Local Execution

Run with any static file server:

```bash
# Python
python -m http.server 3000

# Node.js
npx serve .
```
Open `http://localhost:3000` in your browser.

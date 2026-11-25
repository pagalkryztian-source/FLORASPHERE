# 🌸 3D Flower Gallery

A collection of 10 interactive 3D flowers that run in the browser. Each flower is a single self-contained HTML file built with [Three.js](https://threejs.org/). There is no build step, no `npm install`, and no assets to download.

## The Flowers

| # | File | Flower |
|---|------|--------|
| 1 | `Flower1.html` | Wildflower Meadow |
| 2 | `Flower2.html` | Botanical Azalea |
| 3 | `Flower3.html` | Sacred Lotus |
| 4 | `Flower4.html` | Bioluminescent Blue Spider Lily |
| 5 | `Flower5.html` | Delphinium Garden |
| 6 | `Flower6.html` | Botanical Bigleaf Hydrangea |
| 7 | `Flower7.html` | Lily of the Valley |
| 8 | `Flower8.html` | Globe Amaranth (*Gomphrena globosa*) |
| 9 | `Flower9.html` | Rose |
| 10 | `Flower10.html` | Floating Tulip |

## Features

- **Fully 3D and interactive**: drag to orbit, scroll or pinch to zoom.
- **Procedurally built geometry**: flowers are generated in code, with no imported models or textures.
- **Image-based lighting**: uses Three.js `RoomEnvironment` for realistic reflections.
- **Bloom post-processing** on the Bioluminescent Blue Spider Lily (`Flower4`).
- **Gallery navigation**: `<` and `>` arrows on every page loop through all 10 flowers (10 → 1 wraps around).
- **"Send to someone" button**: copies a direct link to the current flower to your clipboard.
- **Single file per flower**: copy any one HTML file anywhere and it works.

## Getting Started

1. Clone or download this repo:
   ```bash
   git clone https://github.com/<your-username>/<your-repo>.git
   cd <your-repo>
   ```
2. Open any `FlowerN.html` in a modern browser.

If your browser blocks anything when opening files directly, serve the folder locally instead:

```bash
# Python
python -m http.server 8000

# or Node
npx serve .
```

Then visit `http://localhost:8000/Flower1.html`.

## Live Demo (GitHub Pages)

To host the gallery and make the **Send to someone** button useful:

1. Go to **Settings → Pages**.
2. Under **Source**, choose your main branch and the root folder.
3. Your flowers will be live at `https://<your-username>.github.io/<your-repo>/Flower1.html`.

The share button builds its link from the current page URL, so it copies a public link when hosted and a local path when opened from disk.

## Controls

| Action | Desktop | Touch |
|--------|---------|-------|
| Rotate | Left-click + drag | One-finger drag |
| Zoom | Scroll wheel | Pinch |
| Next / previous flower | `>` / `<` arrows | Tap arrows |
| Copy share link | **Send to someone** button | Tap button |

## Tech Stack

- [Three.js](https://threejs.org/) `0.160.0`, loaded from [unpkg](https://unpkg.com/) via an import map
- Three.js add-ons: `OrbitControls`, `RoomEnvironment`, `BufferGeometryUtils` (and `EffectComposer`, `UnrealBloomPass`, `OutputPass` for Flower4)
- Plain HTML, CSS and JavaScript (ES modules)

## Requirements

- A modern browser with **WebGL** support (Chrome, Edge, Firefox, Safari)
- An **internet connection**, since Three.js is loaded from a CDN. If it is blocked or offline, the page won't render the 3D scene.

## Project Structure

```
.
├── Flower1.html
├── Flower2.html
├── ...
├── Flower10.html
└── README.md
```

## Customizing

Each file is independent, so you can edit one without affecting the others. To change a flower's look, open its HTML file and edit the colors and geometry parameters inside the `<script type="module">` block.

## License

Add your preferred license here (for example, MIT).

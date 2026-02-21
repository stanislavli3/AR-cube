# AR Cube

A minimal web app to view a 3D model in the browser and in AR. Built with Lehigh University branding — clean, minimal, and responsive.

**Live:** [https://stanislavli3.github.io/AR-cube/](https://stanislavli3.github.io/AR-cube/)

## Features

- **Inline 3D viewer** — Rotate and zoom the model in the browser (Safari has best support for USDZ).
- **View in AR** — On iPhone and iPad, tap “View in AR” to place the model in your space with AR Quick Look.
- **Responsive** — Works on desktop and mobile with a single, adaptive layout.

## Run locally

Serve the folder over HTTP (required for the 3D model to load; `file://` may be blocked):

```bash
# Python 3
python3 -m http.server 8000

# or Node (npx)
npx serve .
```

Open `http://localhost:8000` in your browser.

## Project structure

| File              | Purpose                          |
|-------------------|----------------------------------|
| `index.html`      | Single-page app and styles       |
| `Archive.glb.usdz`| 3D model (USDZ for AR / Safari)  |
| `image.png`       | Lehigh University logo           |

## AR requirements

- **iOS:** iPhone or iPad with AR support; open the site in Safari and tap “View in AR.”
- **Android:** Limited; inline viewer may work in Chrome; AR experience depends on device and browser support.

No build step or dependencies — just static HTML, CSS, and [model-viewer](https://modelviewer.dev/) loaded from a CDN.

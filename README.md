# GIS Portfolio — Adam Barker

A clean, professional multi-page HTML portfolio for showcasing GIS projects.

## Folder structure

```
gis-portfolio/
├── index.html                         ← Home page
├── capital-improvement-project.html   ← CIP project page
├── urban-infill.html                  ← Infill project page
├── SNAP.html                          ← SNAP project page
├── css/
│   └── style.css                      ← All styles — edit colours/fonts here
├── js/
│   └── main.js
└── img/
    ├── avatar.jpg                     ← My headshot
    ├── CIP-1.jpg                      ← Project screenshots
    ├── infill-1.jpg                   ← Project screenshots
    ├── snap-1.jpg                     ← Project screenshots
    └── ...
```

## Running locally

Since this is plain HTML you have two easy options:

**Option 1 — Python (recommended, already installed on most machines)**
```bash
cd gis-portfolio
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

**Option 2 — VS Code Live Server extension**
Install the "Live Server" extension, right-click `index.html` → Open with Live Server.

> ⚠️ Don't just double-click index.html to open it — the Leaflet map and GeoJSON
> fetch calls require a local server (file:// URLs block them).

## Adding a new project

1. Copy `project-green-space.html` → rename it (e.g. `project-flood.html`)
2. Update the title, description, tags, map centre, and screenshot paths inside the file
3. Add a new card to the `projects-grid` section in `index.html` pointing to the new page

## Adding a Leaflet map to a project page

In the `<script>` block at the bottom of any project page:

```js
// Change the centre coordinates and zoom for your study area
const map = L.map('project-map').setView([LAT, LNG], ZOOM);

// Load your own GeoJSON layer
fetch('data/my-layer.geojson')
  .then(r => r.json())
  .then(data => {
    L.geoJSON(data, {
      style: { color: '#2563eb', fillOpacity: 0.4 }
    }).addTo(map);
  });
```

Put your `.geojson` files in a `data/` subfolder.

## Customising

| What                | Where                          |
|---------------------|--------------------------------|
| Name / bio          | `index.html` hero section      |
| Skills badges       | `index.html` skills section    |
| Contact links       | `index.html` contact section   |
| Accent colour       | `css/style.css` → `--clr-accent` |
| Font                | `css/style.css` → `--font`     |

## Deploying publicly (free options)

- **GitHub Pages** — push the folder to a repo, enable Pages in Settings
- **Netlify** — drag the folder onto netlify.com/drop
- **Vercel** — `npx vercel` in the folder (no build step needed for plain HTML)

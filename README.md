# Adam Barker — GIS Portfolio

A personal GIS portfolio showcasing spatial analysis projects, geospatial workflows, and infrastructure mapping work.

**Live site:** [a-barker.github.io/portfolio](https://a-barker.github.io/portfolio)

---

## About

I'm a Systems Administrator turned GIS analyst, building geospatial workflows with ArcGIS Pro, ModelBuilder, and spatial analysis. This portfolio highlights projects that combine data integrity, repeatable processes, and scalable solutions.

---

## Projects

### Capital Improvement Planning Dashboard — Castle Rock, CO
A GIS-based Capital Improvement Planning dashboard built for Castle Rock, CO. Field technicians collect infrastructure condition data using Survey123 on mobile devices, submissions feed into ArcGIS Online, results are visualized in an Experience Builder dashboard, and data is exported to QGIS and published as a public webmap.

**Tools:** ArcGIS Pro · ArcGIS Online · Survey123 · Experience Builder · QGIS  
**Data:** Douglas County CO GIS · Town of Castle Rock Data Catalog · OpenStreetMap

---

### Las Vegas Residential Infill Potential Analysis
A parcel-level analysis of residential development capacity in Clark County, Nevada. Built in ArcGIS Pro using ModelBuilder, integrating parcel, zoning, dwelling unit, and constraint datasets to identify where new housing could realistically be added within the existing city. Presented as a story map.

**Tools:** ArcGIS Pro · ModelBuilder · Story Maps  
**Data:** U.S. Census Tract · City of Las Vegas GeoCommons · Clark County GIS Management Office · City of Las Vegas Open Library

---

### SNAP Access Analysis *(in progress)*
Using U.S. Census data to analyze SNAP access across geographic areas.

**Tools:** QGIS · Python

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML, CSS, JavaScript |
| Mapping | Leaflet.js, QGIS Cloud |
| Fonts | Inter, Merriweather (Google Fonts) |
| Hosting | GitHub Pages |

---

## Folder Structure

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

---

## Running Locally

**Option 1 — Python**
```bash
cd gis-portfolio
python -m http.server 5500
# Then open http://localhost:5500 in your browser
```

**Option 2 — VS Code Live Server**  
Install the "Live Server" extension, right-click `index.html` → Open with Live Server.

> ⚠️ Don't open `index.html` by double-clicking — the Leaflet map and GeoJSON fetch calls require a local server.

---

## Contact

**Email:** barker.a@gmail.com  
**LinkedIn:** [linkedin.com/in/adam-barker-gis-analyst](https://linkedin.com/in/adam-barker-gis-analyst)  
**GitHub:** [github.com/a-barker](https://github.com/a-barker)

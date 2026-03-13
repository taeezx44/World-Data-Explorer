# 🌍 World Data Explorer

An interactive world map that lets you explore global data — GDP, population, life expectancy, and land area — with smooth animations and real-time metric switching.

![World Data Explorer Preview](https://img.shields.io/badge/Status-Live-4f9cf9?style=flat-square) ![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white) ![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black) ![D3.js](https://img.shields.io/badge/D3.js-F9A03C?style=flat-square&logo=d3.js&logoColor=white)

---

## ✨ Features

- **Interactive Map** — Hover any country to see an instant data tooltip
- **4 Metrics** — Switch between GDP, Population, Life Expectancy, and Area
- **Animated Color Scale** — The entire map recolors with smooth transitions when switching metrics
- **Country Detail Panel** — Click any country to see full stats, comparative bar charts, and a global top 10 ranking
- **Zoom & Pan** — Navigate the map freely with mouse scroll or zoom buttons
- **70+ Countries** — Covers major economies across all continents

---

## 🛠️ Built With

| Technology | Purpose |
|---|---|
| **HTML5** | Page structure and layout |
| **CSS3** | Dark theme UI, animations, responsive design |
| **Vanilla JavaScript** | State management, data binding, event handling |
| **D3.js v7** | Map projection, geo rendering, color scales, zoom |
| **world-atlas** | TopoJSON world geometry data (via CDN) |
| **topojson** | Converting TopoJSON to GeoJSON features |

> No framework. No build step. Just open the file and it works.

---

## 🚀 Getting Started

### Option 1 — Open directly
```bash
# Just open the file in any browser
open world-data-explorer.html
```

### Option 2 — Serve locally (recommended to avoid CORS issues)
```bash
# Python
python -m http.server 8000

# Node.js
npx serve .
```
Then visit `http://localhost:8000`

### Option 3 — Deploy to Netlify
1. Rename `world-data-explorer.html` → `index.html`
2. Drag the folder into [Netlify Drop](https://app.netlify.com/drop)
3. Get a live URL instantly

---

## 📊 Data Coverage

Data sourced from World Bank and UN estimates (2022–2023).

| Metric | Unit | Countries |
|---|---|---|
| GDP | USD Billion | 75+ |
| Population | Million people | 75+ |
| Life Expectancy | Years | 75+ |
| Area | Thousand km² | 75+ |

---

## 🗂️ Project Structure

```
world-data-explorer/
│
├── index.html          # Everything — styles, markup, and scripts in one file
└── README.md           # This file
```

This is intentionally a single-file project to make it easy to share, deploy, and embed anywhere.

---

## 🧠 How It Works

```
User hovers country
    → D3 fires mousemove event
    → Numeric country ID is resolved to ISO3 code
    → Country data is looked up from the in-memory dataset
    → Tooltip renders with interpolated values

User switches metric
    → Color scale is recomputed using d3.scaleQuantile
    → All country paths are re-filled with new colors
    → Sidebar top 10 list updates to match new metric
```

---

## 🔮 Roadmap

- [ ] Add time slider to show data changes over years
- [ ] Mobile touch support for pan/zoom
- [ ] Search bar to jump to any country
- [ ] Compare mode — select two countries side by side
- [ ] Export chart as PNG

---

## 📄 License

MIT — free to use, modify, and share.

---

<p align="center">Built with D3.js and zero frameworks 🗺️</p>

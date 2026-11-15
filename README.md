# 🌿 Ofoiq (أفق) — Al-Nasariya Agricultural Digital Twin Platform | NASA Space Apps Challenge

An intelligent, data-driven agricultural decision-support web platform and 3D Digital Twin built for farmers and decision-makers in **Al-Nasariya (Nablus, Palestine)** (`32.2438° N, 35.3900° E`). Powered by daily agro-climatological data from **NASA POWER (v2.10.3)** covering the 120-day summer-to-autumn transition window (**July 15 – November 11, 2026**) alongside live 7-day weather forecasts.

---

## 🚀 Live Demo
🌐 **[View Live Web Application](https://nasa-ofoiq-team.github.io/NasaOfoiq-project/)**

---

## ✨ What's New & Key Functionalities

- 🧊 **Upgraded 3D Digital Twin Environment (Three.js r128):**
  - Realistic terraced Palestinian agricultural landscape featuring limestone retaining walls (*Salasil*), procedural soil textures with furrow geometry, and olive trees.
  - 3 distinct instanced crop geometries (**Cereals**, **Legumes**, and **Cover Crops**) that dynamically grow, sway with wind speed (`WS10M`), change color under heat/moisture stress, and ripen based on thermal accumulation.
  - Interactive 3D farm infrastructure: clickable **Drip Irrigation Valves** per sector ($A, B, C$), **Farm Water Cistern/Tank** with dynamic water levels, **Ground Weather & Soil Sensor Mast**, greenhouse/mulch tunnels, and floating 3D world pins.
- 👨‍🌾 **Dual-Mode Interface (Farmer-First vs. Expert & Simulation):**
  - **Farmer Mode (`واجهة المزارع`):** Simplified daily action plan featuring a practical **Irrigation Valve Timer** (exact minutes and $m^3$ tailored by dunam area) and one-click auto-pilot execution.
  - **Expert Mode (`وضع الخبير والمحاكاة`):** Interactive 120-day agro-climate timeline chart, crisis simulators (**Heatwave 42°C** & **Heavy Rain 18.5 mm**), and seasonal ROI estimators.
- 🛰️ **NASA POWER v2.10.3 Integration & Scientific Quality Screening:**
  - Real-time analysis of Surface Soil Wetness (`GWETTOP`), Bias-Corrected Precipitation (`PRECTOTCORR`), Max/Min/Mean Temperatures (`T2M_MAX`, `T2M_MIN`, `T2M`), Relative Humidity (`RH2M`), and Wind Speed (`WS10M`).
  - **Methodological Alignment:** Root-zone wetness (`GWETROOT`) is explicitly flagged as under verification and excluded from active resilience scoring due to its Oct 1 step discontinuity in POWER v2.10.3.
- 📈 **Validated Agro-Climate Models:**
  - **Hargreaves-Samani $ET_0$ & Water Deficit:** Daily reference evapotranspiration and net irrigation requirement calculations ($\max(0, ET_0 - P)$).
  - **Crop Resilience Index (CRI):** Weighted index combining 7-day rainfall trends, thermal stress thresholds ($T_{\max} \ge 35^\circ\text{C}$), and surface soil moisture (`GWETTOP`).
  - **Growing Degree Days (GDD):** Thermal unit accumulation tracker ($T_{\text{base}} = 5^\circ\text{C}$, maturity target $1350\text{ GDD}$) with interactive growth-stage scrubbing.
- ⚖️ **3-Strategy Crop Rotation Comparator:** Side-by-side 3-season comparison between **Ofoiq Balanced Rotation** (Legumes → Wheat → Cover Crop), **Drought-Resilient Rotation** (Barley/Legumes/Cover), and **Traditional Cereal Monoculture**.
- 🗺️ **Soil Moisture Heatmap & Transparent Roadmap:** Toggleable 3D soil heatmap highlighting edge evaporation vs. core moisture retention, plus transparent labeling of simulated/planned integrations (`Sentinel-2` NDVI sector simulation, `SMAP`/`GLDAS`, `ECOSTRESS`, and experimental pest risk indexing).

---

## 🛠️ Tech Stack & Dependencies

- **Core Languages:** HTML5 / CSS3 / Vanilla JavaScript (ES6+)
- **3D Graphics Engine:** [Three.js](https://threejs.org/) (`r128` via CDN) with `ACESFilmicToneMapping`, soft shadows, and instanced meshes
- **UI/UX & Styling:** Google Fonts (`Cairo`), RTL Arabic layout, Glassmorphism UI, and magnetic proximity micro-interactions
- **Data Sources:** NASA POWER API v2.10.3 (`32.2438° N, 35.3900° E`) & Open-Meteo 7-Day Forecast API

---

## 📁 Project Structure

```text
.
├── index.html       # Single-file core web app (HTML5, Glassmorphic CSS, Three.js 3D Twin & Agro-Climate Engine)
├── data.json        # Supplemental NASA space-guided resilient action plans
└── README.md        # Technical documentation, scientific alignment & feature overview

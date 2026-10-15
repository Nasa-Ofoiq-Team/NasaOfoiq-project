# 🌿 Al-Nasariya Agricultural Digital Twin Platform | NASA Space Apps Challenge

An intelligent, data-driven agricultural decision-support web platform and 3D Digital Twin built for farmers and decision-makers in the **Al-Nasariya region (Nablus)**. Powered by historical spaceborne climate data from **NASA POWER** (September – December 2022).

---

## 🚀 Live Demo
🌐 **[View Live Web Application](https://nasa-ofoiq-team.github.io/NasaOfoiq-project/)**

---

## ✨ Features & Key Functionalities

* 🧊 **Interactive 3D Digital Twin Scene (Three.js Engine):** Real-time 3D visualization of 3 farm plots ($A, B, C$) with dynamic crop growth, field irrigation sprinklers, organic mulching/cover simulation, and interactive 3D warning alert icons ($⚠️$).
* 🛰️ **NASA POWER Data Integration:** Real-time analysis of Surface Soil Wetness (`GWETTOP`), Root-Zone Wetness (`GWETROOT`), Precipitation (`PRECTOTCORR`), Max/Min Temperatures (`T2M_MAX`/`T2M_MIN`), and Relative Humidity.
* 📈 **Crop Resilience Index (CRI):** Dynamic calculation merging 7-day rainfall trends, soil temperature, and surface/root soil moisture to measure real-time crop health resilience.
* 🎯 **Goal-Driven Strategy Engine:** Interactive scenario switching between **Water Conservation** (💧), **Maximum Yield** (📈), and **Drought Resistance** (☀️).
* 🧮 **Financial & Water ROI Calculator:** Real-time estimations of water savings ($m^3$) and financial yield increase ($$) using Hargreaves evapotranspiration equations tailored by dunam acreage.
* 🔄 **3-Season Crop Rotation Simulator:** Interactive multi-season planning engine demonstrating soil nitrogen recovery across legumes, cereals, and fallow cycles.
* 📱 **Mobile-First Responsive Layout:** Fluid viewport scaling designed to work seamlessly on smartphones, tablets, and desktop displays.

---

## 🛠️ Tech Stack & Dependencies

* **Core Language:** HTML5 / CSS3 / JavaScript (ES6+)
* **3D Graphics Engine:** [Three.js](https://threejs.org/) (r128 via CDN)
* **Typography & Styling:** Google Fonts (Cairo) & Pure Responsive CSS3
* **Data Sources:** NASA POWER API Climate Dataset (Al-Nasariya, Nablus coordinates)

---

## 📁 Project Structure

```text
.
├── index.html       # Single-file core web app (HTML5, Responsive CSS, Three.js & Logic)
├── data.json        # Supplemental NASA space-guided resilient action plans
└── README.md        # Technical project documentation & overview

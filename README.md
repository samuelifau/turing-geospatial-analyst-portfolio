<div align="center">

# 🌊 **Flood Risk Analysis — Denpasar, Bali**
### 🛰️ Geospatial • Remote Sensing • Python • AI Model Evaluation

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)]()
[![Rasterio](https://img.shields.io/badge/Rasterio-GIS-green)]()
[![Geopandas](https://img.shields.io/badge/Geopandas-Vector-orange)]()
[![QGIS](https://img.shields.io/badge/QGIS-3.34-brightgreen?logo=qgis)]()
[![Remote Sensing](https://img.shields.io/badge/Remote%20Sensing-SRTM-yellow)]()
[![License](https://img.shields.io/badge/License-MIT-purple)]()

</div>

---

<p align="center">
  <img width="641" height="641" alt="image" src="https://github.com/user-attachments/assets/7dee86b7-b1bf-4983-b045-85db00d51fc1" />
</p>


## 📌 **Overview**
This project generates a **Flood Risk Map** for **Denpasar, Bali**, using a complete geospatial pipeline:

- ✔ SRTM 30m DEM (USGS)  
- ✔ OSM River Network (cleaned + converted)  
- ✔ Python processing → Rasterio, Geopandas, Numpy  
- ✔ Terrain modeling → elevation, slope, river distance  
- ✔ Adaptive flood scoring (1–4)  
- ✔ Vector polygon output (GPKG)  
- ✔ Debug notebook with error-safe file operations  

> 🎯 **Designed for Geospatial RLHF / AI Evals and GIS Analyst roles.**

---

## 🗂 **Data Sources**

| Dataset | Source | Status |
|--------|--------|--------|
| 🌄 **DEM (SRTM 30m)** | USGS / Google Earth Engine | Preprocessed, clipped, UTM-corrected |
| 🌊 **River Network** | OpenStreetMap | Cleaned, field-filtered, CRS-fixed |
| 🗺 **Study Area** | Derived from DEM | Matches entire Denpasar region |

Raw data located in:

---

## 🧠 **Workflow Diagram**

      DEM (SRTM)                 Rivers (OSM)
           │                           │
           ▼                           ▼
    Clip & Reproject            Clean Fields
           │                           │
           ▼                           ▼
       Elevation                 Rasterize Rivers
           │                           │
           ├──────────┬────────────────┘
           ▼          ▼
       Slope      Distance-to-River
           │               │
           └───────┬──────┘
                   ▼
       Adaptive Risk Scoring (1–4)
                   │
                   ▼
  🗺️  Flood Risk Map + Vector Polygons


---

## 🌈 **Risk Class Legend (1–4)**

| Class | Level | Color |
|-------|--------|--------|
| **1** | 🟩 Low | `#2ecc71` |
| **2** | 🟨 Moderate | `#f1c40f` |
| **3** | 🟧 High | `#e67e22` |
| **4** | 🟥 Very High | `#c0392b` |

---

## 🗺 **Output Preview**

### 🌀 **Final Flood Risk Map (PNG)**  

<p align="center">
  <img width="641" height="641" alt="image" src="https://github.com/user-attachments/assets/7dee86b7-b1bf-4983-b045-85db00d51fc1" />
</p>

🔍 Hillshade + transparency → gives intuitive terrain context  
🎨 4-Level discrete colorbar included (Low → Very High)  

---

## 📦 **Generated Outputs**

### 📁 Raster outputs (`data/processed/`)
- `dem_clip.tif`
- `dem_utm.tif`
- `slope.tif`
- `dist_to_river.tif`
- `risk_index.tif`
- `risk_class.tif`

### 🗂 Vector outputs (`outputs/shapefiles/`)
- `denpasar_flood_risk_zones.gpkg`  
  ✔ Multipolygon per risk class (1–4)  
  ✔ Ready for GIS apps (QGIS, ArcGIS, Kepler.gl)

---

## 📘 **Notebook**
Main notebook (debug-friendly):


Contains:
- DEM processing  
- River cleaning  
- Raster math  
- Polygonization  
- Error-handling (safe_remove)  
- Full reproducible pipeline  

---

## 🧪 **QA/QC Checks**

| Check | Status |
|-------|--------|
| CRS validation | ✔ EPSG:4326 → UTM50S |
| Nodata handling | ✔ Cleaned & enforced |
| Slope sanity | ✔ 0–40° typical in Denpasar |
| Distance distribution | ✔ Verified percentiles |
| Unique classes | ✔ 1–4 only |
| Vector topology | ✔ Valid polygons |

---

## 🎯 **Skills Demonstrated**

- Geospatial reasoning & interpretation  
- Remote sensing preprocessing  
- Python raster/vector workflows  
- Spatial classification  
- Terrain analysis  
- CRS & projection handling  
- GIS QA/QC  
- AI/Evals-style spatial consistency checking  

---

## 👤 **Author**
**Samueli Windovado Fau**  
🌐 GitHub: https://github.com/samuelifau  
💼 LinkedIn: https://www.linkedin.com/in/samueli-fau  

---

<div align="center">

### ⭐ If you find this project helpful, please star the repo!  
It supports my application for **Geospatial RLHF / GeoAI roles**.

</div>



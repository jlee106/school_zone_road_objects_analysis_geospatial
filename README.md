# 🗺️ Geospatial Analysis of Road Safety Objects Around School Zones in Singapore

## 📖 Overview
This project explores the spatial distribution of **road safety features** (road crossings, road humps, speed regulating strips, traffic signs, and word markings) around **school zones in Singapore**.

The goal is to identify schools that may have fewer safety infrastructures, using open geospatial data. This analysis serves as a preliminary step toward understanding whether schools with fewer safety features face higher traffic accident risks.

---

## 🎯 Objectives
- Analyse the number and types of road safety objects around school zones.  
- Identify schools with low counts of safety features.  
- Build a foundation for future correlation analysis between **accidents** and **infrastructure density**.

---

## 🧭 Project Flow
1. **Introduction** – Motivation for studying school zone safety.  
2. **Context** – Overview of Singapore’s transport data (fatalities, injuries, car population).  
3. **Analysis** – Counting and visualising road objects around school zones (Dashboarding using Power BI).  
4. **Limitations** – Acknowledging data and methodological constraints.  
5. **Recommendations** – Directions for deeper analysis and policy application.  

---

## 🧩 Data Sources
| Dataset | Description | Source |
|----------|--------------|--------|
| School zones | Geospatial polygons of school areas | [LTA Data Mall](https://datamall.lta.gov.sg/content/datamall/en/static-data.html#Whole%20Island) |
| Road Objects | Geospatial line or points | [LTA Data Mall](https://datamall.lta.gov.sg/content/datamall/en/static-data.html#Whole%20Island) |
| Transport statistics | Traffic casualties, road length, car population | [data.gov.sg](https://data.gov.sg) |

*(Note: Replace with actual dataset links once confirmed.)*

---

## 🧠 Methodology
1. **Data Cleaning & Standardisation**  
   - Ensured consistent CRS (`EPSG:3414` for Singapore SVY21).  

2. **Spatial Join & Buffering**  
   - Created 100m  buffers around each school zone (e.g., 100m–150m).  
   - Used spatial joins to locate road objects within  

3. **Exploratory Analysis & Visualisation**  
   - Histograms and boxplots to show distribution of safety features.  
   - PowerBI dashboard for traffic accident & road data, and each road object type
   - Identified school zones with most road objects and school zones with least.

---

## 📊 Key Visualisations
- **Histogram:** Distribution of total safety features across schools.  
- **Map:** Interactive map on PowerBI to show spatial distribution of schools.  
- **Bar Chart:** Breakdown of object types per school.  

---

## ⚠️ Limitations
- Datasets may be incomplete or not updated regularly.  
- Buffer-based proximity may not capture traffic exposure or road hierarchy.  
- Focused only on school zones; does not establish causality with accidents.

---

## 💡 Future Work
- Correlate accident occurrence data with safety object density.  
- Incorporate traffic volume, pedestrian counts, or school size.  
- Develop a **School Safety Index** based on spatial risk factors.  
- Extend analysis to other sensitive zones (e.g., silver zones).

---

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:**  
  - `geopandas`, `pandas`, `matplotlib`, `numpy`  
- **Environment:** Jupyter Notebook
- **Visualisation Tool:** Power BI

---

## 📁 Repository Structure

| Folder            | Description                                                                  |
| ----------------- | ---------------------------------------------------------------------------- |
| **data/**         | Contains raw and cleaned datasets used for analysis.                         |
| **notebooks/**    | Includes Jupyter notebooks for data cleaning and geospatial processing.      |
| **dashboard/**    | Contains the Power BI dashboard file for interactive visualisation.          |
| **presentation/** | Stores the final presentation deck summarising key findings.                 |


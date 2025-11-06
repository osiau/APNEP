# APNEP Spatial Targeting Repository

## Purpose

This repository organizes and documents all spatial data used to build the **APNEP Spatial Targeting Framework**, which integrates ecological and social indicators to identify areas that are most suitable for **wetland conservation, enhancement (restoration), and community resilience**.

The goal is to ensure transparent, reproducible, and accessible workflows that support data-driven decision-making for environmental planning in the **Albemarle-Pamlico National Estuary Partnership (APNEP)** region.

---

## Folder Structure

```
APNEP/
├─ inputs/
│  ├─ boundaries/
│  ├─ crpa/
│  └─ wsi/
└─ outputs/
   ├─ boundaries/
   ├─ crpa/
   ├─ wsi/
   │  ├─ conserve/
   │  ├─ enhance/
   │  └─ combined/
   └─ opportunity/
```

---

## Folder Descriptions

### **inputs/**

Contains all input data layers used to build the Wetland Suitability Index (WSI), Community Resilience Priority Areas (CRPA), and Opportunity Area analyses.

* **boundaries/** – Administrative and physical boundaries (e.g., APNEP region, counties, basins, roads).
* **crpa/** – Inputs used to create the CRPA model, including disadvantage, FUTURES 3.0 development pressure, and low local capacity data.
* **wsi/** – Inputs used in WSI analyses (wetlands, slope, soil drainage, barriers, contaminated land).

---

### **outputs/**

Contains all processed, cleaned, and final analysis layers ready for mapping or statistical use.

* **boundaries/** – Final, clipped, or merged boundary files used for summaries or visualization.
* **crpa/** – Composite CRPA layers and related outputs showing social and environmental vulnerability.
* **wsi/** – Wetland Suitability Index results, including conservation, enhancement, and combined indices.

  * **conserve/** – WSI conservation results and high-suitability zones.
  * **enhance/** – WSI enhancement (restoration) results and high-suitability zones.
  * **combined/** – Combined conservation and enhancement layers and PAD-US masked versions.
* **opportunity/** – Overlap layers showing where high ecological suitability and social vulnerability coincide, with PAD-US masking applied to exclude protected lands.

---

## Metadata

All datasets are documented in a single **metadata Excel sheet** (`apnep_metadata.xlsx`) located at the root of the repository.
Each row corresponds to one dataset and includes essential information for citation, tracking, and reproducibility.

| **Field Name**          | **Description**                                                                        |
| ----------------------- | -------------------------------------------------------------------------------------- |
| **Filename(.zip)**            | Exact filename of the dataset (e.g., `apnep-wsi-conserve-v251104.tif`).                |
| **Dataset Name**        | Plain-English title of the dataset (e.g., “Wetland Suitability Index – Conservation”). |
| **Repository Folder**   | Folder location within the repo (e.g., `outputs/wsi/conserve/`).                       |
| **File Type**           | Data format such as `raster`, `vector`, or `table`.                                    |
| **Processing Notes**    | Short summary of key data processing steps, sources, and classification rules.         |
| **CRS**                 | Coordinate Reference System used (e.g., `EPSG:32119 – NAD 1983 / North Carolina`).     |
| **Citation (optional)** | Full data citation or online source reference.                                         |

The metadata sheet ensures all datasets are traceable, versioned, and properly cited.

---

## Coordinate Reference System

All data are standardized to **EPSG:32119 (NAD 1983 / North Carolina)** for regional analysis.
Some data may be in their original crs or **EPSG:4326 (WGS 84)**.

---

## Major Dataset Themes

### **Wetland Suitability Index (WSI)**

Identifies areas suitable for wetland **conservation** and **enhancement (restoration)** using ecological indicators such as slope, soil drainage, riparian buffers, and land-use barriers.

* `apnep-wsi-conserve`, `apnep-wsi-enhance`, `apnep-wsi-combined`
* Associated inputs: `apnep-wsi-slope`, `apnep-wsi-soildrainage`, `apnep-wsi-contaminated`, etc.

### **Community Resilience Priority Areas (CRPA)**

Highlights communities facing high environmental and social vulnerability using combined layers of disadvantage, low local capacity, and future development pressure.

* `apnep-crpa`, `apnep-crpa-disadvantage`, `apnep-crpa-futures3`, `apnep-crpa-lowlocalcap`

### **Opportunity Areas**

Defines locations where ecological and social priorities overlap — specifically, where high-suitability WSI zones intersect CRPA high-priority areas, with PAD-US masking to remove protected lands.

* `apnep-oppareas-padusmask`

### **Boundaries**

Includes geographic boundaries used to clip, summarize, and visualize data.

* `apnep-bnd-boundary` (APNEP region)
* `apnep-bnd-counties` (County boundaries)
* `apnep-bnd-roads` (Major roads)

---


## Data Use & Licensing

All datasets in this repository are derived from **public domain** or **open government data** sources.
Users may freely reproduce, modify, and distribute these data with appropriate citation of original sources.

---

## Contact

**Maintainer:** Uchenna Osia
Ph.D. Candidate, North Carolina State University
Email: [[unosia@ncsu.edu](mailto:your-email@ncsu.edu)]

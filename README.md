# District-wise Participation Heatmap
## Maharashtra Mental Health Sensitisation Programme — DMER × iCALL, TISS

An interactive choropleth map visualising district-level medical student participation in a statewide mental health sensitisation programme across Maharashtra, India. Built in Python as part of data reporting and programme evaluation work at [iCALL, Tata Institute of Social Sciences (TISS)](https://icallhelpline.org/).

---

## Research context

This visualisation was developed to support the **DMER Maharashtra × iCALL, TISS Mental Health Sensitisation Programme** — a state-level initiative to improve mental health literacy, build sensitisation and reduce stigma among medical students and faculty enrolled in 24 government medical colleges across Maharashtra (2025).

Understanding the geographic distribution of participation matters for two reasons:

1. **Programme monitoring** — identifying districts with lower reach helps mental health programmers target programmes and  outreach to allocate resources more effectively
2. **Policy communication** — presenting district-level coverage in an accessible visual format for state-level stakeholders, including the Directorate of Medical Education and Research (DMER)

The map renders districts with programme coverage on an orange-to-red intensity scale (higher participation = deeper red) and districts with no reach to any government medical college in the sample in grey, clearly distinguishing programme reach from geographic gaps.

---

## Data

| Detail | Description |
|---|---|
| **Source** | Programme administrative records — DMER Maharashtra × iCALL, TISS (2025) |
| **Unit of analysis** | District |
| **Variable visualised** | Number of medical students who were reachable and participated in mental health sensitisation sessions from different medical colleges across the state|
| **Coverage** | 24 government medical colleges across Maharashtra |
| **Geographic boundaries** | Maharashtra district-level GeoJSON (all 36 districts) |

> The participation data is from a programme evaluation study and is not publicly available. See [`data/data_sources.md`](data/data_sources.md) for full details.

---
## Methods
- Data loading and preprocessing with `pandas` and `geopandas`
- District name standardisation and mismatch checking across datasets (including handling Maharashtra's 2023 district renaming)
- Left merge of geospatial boundary data with participation data
- Custom colour scale with sentinel value approach for missing districts (grey fill)
- Interactive choropleth built with `plotly.express`
- Export as standalone HTML (offline-compatible) and static PNG
---
## Repository structure

```
Maharashtra-Interactive-Heatmap/
├── maharashtra_heatmap.ipynb   # Annotated source notebook (full workflow)
├── maharashtra_heatmap.html    # Interactive output — download and open in browser
├── maharashtra_heatmap.png     # Static map for reports/presentations
├── data/
│   └── data_sources.md         # Data provenance and access notes
└── README.md
```
---
## How to run

1. Clone this repository
2. Obtain the data files as described in `data/data_sources.md`
3. Place the CSV and GeoJSON files in the `data/` folder
4. Open `maharashtra_heatmap.ipynb` in Google Colab or Jupyter
5. Run all cells in order

**To view the map without running any code:** download `maharashtra_heatmap.html` and open it in any browser.
---
## About

Developed by **Amruta Gaikwad** as part of programme evaluation and data reporting work at iCALL, TISS, Mumbai.  
The broader DMER × iCALL programme evaluation, including pre-post test analyses of mental health sensitisation sessions across 3,000+ students, is described in a manuscript currently in preparation.

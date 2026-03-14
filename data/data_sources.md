# Data Sources

## Participation data

**File:** `Maharashtra_DMER_Student_Outreach.csv`

**Description:** District-level aggregated counts of medical student participation in mental health sensitisation sessions delivered as part of the DMER Maharashtra × iCALL, TISS programme (2023–2025).

**Source:** Programme administrative records, iCALL, Tata Institute of Social Sciences (TISS), Mumbai, in collaboration with the Directorate of Medical Education and Research (DMER), Maharashtra.

**Availability:** This dataset is not publicly available. It was collected as part of a programme evaluation study under institutional oversight at TISS. Requests for access may be directed to iCALL, TISS (https://icallhelpline.org/).

**Variables used:**

| Column | Description |
|---|---|
| `District` | Name of Maharashtra district |
| `N` | Number of students who participated in sensitisation sessions |
| `%` | Percentage of enrolled students who participated |

---

## Geospatial boundary data

**File:** `maharashtra.geojson`

**Description:** District-level administrative boundary polygons for all 36 districts of Maharashtra, India.

**Source:** Publicly available Maharashtra district GeoJSON. Multiple versions are available online; one reliable source is the [Datameet India Maps repository](https://github.com/datameet/maps).

**Note on district names:** Maharashtra officially renamed several districts in 2023 (e.g., Osmanabad → Dharashiv, Aurangabad → Chhatrapati Sambhajinagar). Depending on the GeoJSON version used, names may reflect old or new designations. The notebook includes a name-correction step to handle this. Check the `district` column in your GeoJSON against the participation data and update the `name_corrections` dictionary in the notebook accordingly.

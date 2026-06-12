# Netflix_Catalog_BI_Dashboard
An interactive executive data pipeline and BI dashboard built using Excel Advanced Data Modelling, Power Query ETL, Power Pivot, and custom DAX metrics to analyze global content trends.

# Corporate Data Case Study: Netflix Content Library Optimization & Analytics

## 📊 Executive Interactive Dashboard
Here is the final production-ready executive analytics interface built to track content saturation, licensing velocities, and library demographics.

![Netflix Executive Dashboard](dashboard_final.png)

---

## 🛠️ Advanced Analytics Tool Stack
* **Excel Power Query Engine:** Enterprise Extract, Transform, Load (ETL) pipeline architecture.
* **Excel Data Model (Power Pivot):** In-memory relational database design and schema optimization.
* **Data Analysis Expressions (DAX):** Custom analytical measures overriding flat grid constraints.
* **UI/UX Dashboard Architecture:** Asynchronous data slicing and decoupled multi-layered reporting views.

---

## ⚙️ Technical Deep Dive: The Data Engineering Pipeline

### 1. Robust ETL & Data Normalization (Power Query)
* **The Action:** Ingested 5 separate transactional source worksheets and constructed a unified relational model using optimized **Left Outer Joins** on the primary/foreign identifier `show_id`.
* **The Purpose:** Avoided performance-degrading lookups (like `VLOOKUP`). Kept the operational asset log entirely complete; titles missing peripheral metadata (like unknown production countries) were preserved instead of being dropped by the system.

### 2. Relational Database Modeling (Power Pivot)
* **The Action:** Pushed the unified data arrays into the underlying xVelocity database engine via the **Data Model**, establishing an ironclad data hierarchy.
* **The Purpose:** Addressed the technical hurdle of one-to-many relationships (e.g., titles mapping to multiple distinct genre descriptors). By avoiding a traditional flattened spreadsheet layout, the model eliminates duplicate row weight and protects system memory.

### 3. Advanced Metric Calculations (DAX)
To secure mathematical accuracy across intersecting dimensions, standard counting functions were bypassed in favor of advanced DAX measures:
* **Unique Inventory Volume:** Ensure distinct asset reporting despite dimensional row splits:
```excel
  Unique_Titles := DISTINCTCOUNT(Merge1[show_id])

* **Content Portfolio Freshness:** Calculates the percentage concentration of late-era content releases (2018–2020) relative to historical holdings:
Catalog_Freshness_Pct := DIVIDE(CALCULATE([Unique_Titles], Merge1[release_year] >= 2018), [Unique_Titles])

High-Retention Assets: Flags multi-season television properties driving long-term subscriber lifetime value (LTV):
Bingeable_Shows := CALCULATE([Unique_Titles], Merge1[type]="TV Show", Merge1[duration_seasons] >= 3)

## 📈 Strategic Business Insights Generated
 Velocity Concentration: The 31% Modern Content Ratio proves that nearly one-third of the entire content library was deployed within a tight three-year window (2018–2020). This stands as empirical evidence of aggressive capital deployment during the height of the streaming wars.
 Retention vs Acquisition Engine: While Movies represent 68% of library volume, the identification of 344 deep-inventory TV franchises targets the core operational driver behind recurring monthly billing and user retention.

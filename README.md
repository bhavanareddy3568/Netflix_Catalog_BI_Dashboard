# Netflix_Catalog_BI_Dashboard
An interactive executive data pipeline and BI dashboard built using Excel Advanced Data Modelling, Power Query ETL, Power Pivot, and custom DAX metrics to analyze global content trends.

---

# 🎬 Netflix Content Strategy & Portfolio Optimization Analytics

## 🎯 Executive Summary
* **The Business Challenge:** Netflix spends billions annually on content acquisition and original productions. However, global executives faced a critical operational blindspot: catalog aging (how much of the library is legacy vs. modern), structural balance between high-churn movies and high-retention TV series, and data corruption in tracking metrics that threatened to misguide multi-million dollar licensing decisions.
* **The Solution:** Engineered a centralized, automated Business Intelligence application that unifies fragmented content data streams into a single source of truth, providing leadership with real-time, cross-filtered visibility into library demographics, saturation, and historical acquisition velocities.
* **The Commercial Impact:** Uncovered that **31% of the entire global catalog is hyper-concentrated in just a three-year window**, signaling a massive reliance on continuous production spending. Successfully isolated and mapped the **344 core "bingeable" franchises** that anchor long-term subscriber retention, providing content acquisition teams with a predictive blueprint to optimize future budgets.

---

# Corporate Data Case Study: Netflix Content Library Optimization & Analytics

## 📊 Executive Interactive Dashboard
Here is the final production-ready executive analytics interface built to track content saturation, licensing velocities, and library demographics.

<img width="1869" height="735" alt="Excel_Dashboard" src="https://github.com/user-attachments/assets/d3409254-cfe7-45ee-87ca-85f13cd90c56" />

---

## 🏢 1. The Deep-Dive Business Problem

In the highly competitive streaming landscape, subscriber retention (minimizing churn) is the ultimate metric for profitability. Content strategy teams at Netflix must constantly answer a complex question: *Are we investing our budget in the right mix of content to keep users paying month after month?*

During operations, several roadblocks paralyzed this decision-making process:
1. **Siloed & Fragmented Data Layers:** Critical business dimensions—directors, cast members, category tags, and country logistics—lived in separate database tables. Executives could not easily see the intersection of genre popularity and geographic market availability.
2. **The "Garbage In, Garbage Out" Risk:** A severe row-shifting corruption in the raw transactional logs misaligned text fields into numeric duration columns, skewing average movie runtimes down to an impossible 1.4 minutes. Basing production strategies on these corrupted metrics would lead to deeply flawed investments.
3. **Lack of Dynamic Scenario Analysis:** Leadership lacked a self-service tool to instantly filter library trends by maturity ratings (e.g., targeting adult vs. family demographics) or historical release eras to see what content actually scaled the platform.

---

## 🛠️ 2. The Analytical Solution (How It Was Solved)

To bridge the gap between raw data and executive execution, I designed a multi-layered data infrastructure built for maximum accuracy and zero clutter:

* **Enterprise ETL Pipeline & Normalization:** Using **Power Query**, I extracted and cleansed the fragmented sheets, building structural relationships based on a unique asset key (`show_id`). This kept the inventory asset log 100% complete, ensuring indie films or international titles with missing production metadata were preserved rather than erroneously dropped.
* **Mathematical Integrity Engine:** Because a single title can cross-reference multiple actors or genres, traditional database flattening causes severe row duplication. I bypassed standard spreadsheet calculations by initializing an in-memory **Data Model (Power Pivot)** and coding custom **DAX measures** (like `DISTINCTCOUNT`). This forced the system to report a flawless, uninflated true unique asset volume, protecting the financial credibility of the metrics.
* **Executive Presentation Layer:** Built a clean, dark-themed interactive application interface. By separating raw storage, backend metric grids, and the front-end canvas, the design protects system data from accidental edits while allowing non-technical stakeholders to fluidly navigate complex global data via automated visual controls.

---

## 📊 3. Core Business Insights & Strategic Impact

The application turned raw historical logs into clear operational narratives that answer critical corporate strategy questions:

### A. The "Streaming Wars" Production Treadmill
* **The Finding:** The dashboard revealed a **31.0% Modern Content Ratio** (titles released between 2018–2020). 
* **The Business Impact:** This means nearly one-third of Netflix's entire global inventory was deployed in just a tight 3-year window, compared to the remaining 69% which spans a century of cinematic history. This proves the extreme velocity of capital spending required during the height of the streaming wars. It serves as a warning metric for finance teams: Netflix is on a content "treadmill"—if production velocity slows down, a massive chunk of the platform's perceived value proposition risks feeling stale to consumers.

### B. Monetization Mix: Retention vs. Acquisition
* **The Finding:** The catalog maintains a structural split of **~68% Movies and ~32% TV Shows**. However, the data model successfully isolated exactly **344 "High-Retention" TV Franchises** (series sustaining 3 or more seasons).
* **The Business Impact:** While movies drive initial user acquisition and "buzz," long-form episodic TV series drive subscriber Lifetime Value (LTV). A movie provides 2 hours of engagement; a 4-season TV series locks a user into a recurring monthly billing cycle for weeks. Identifying the precise size and growth curve of these 344 anchor properties allows portfolio managers to balance low-cost legacy titles against high-margin binge assets.

### C. Demographic Target Saturation
* **The Finding:** Dynamic cross-filtering through the audience maturity slicers illustrated that adult-targeted programming (`TV-MA`) experienced a vertical scaling velocity that radically outpaced family-friendly content (`TV-Y`) during Netflix’s global expansion phase.
* **The Business Impact:** This gives regional marketing and procurement teams the exact demographic blueprint that drove historical platform scale, allowing them to align localized licensing budgets with the proven target audience behavior of the platform.

---

## 🛠️ 4. Advanced Analytics Tool Stack
* **Excel Power Query Engine:** Enterprise Extract, Transform, Load (ETL) pipeline architecture.
* **Excel Data Model (Power Pivot):** In-memory relational database design and schema optimization.
* **Data Analysis Expressions (DAX):** Custom analytical measures overriding flat grid constraints.
* **UI/UX Dashboard Architecture:** Asynchronous data slicing and decoupled multi-layered reporting views.

---

## 🎯 5. Professional Skill Tags Demonstrated
* **Strategic Portfolio Analysis**
* **Data-Driven Storytelling**
* **Business Intelligence (BI) Architecture**
* **Data Quality Assurance & Auditing**
* **Executive Reporting Systems**
* **Relational Database Design**

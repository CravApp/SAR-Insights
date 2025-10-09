🌲 SAR INSIGHTS: Detection of Subtle Forest Degradation (Amazon)
Hackathon: 14 Hours of Flawless Execution
🌐 MVP PLATFORM (Demo): https://www.sar-insights.lat
🎯 THE PROBLEM AND THE SOLUTION
| Area | Description |
|---|---|
| Core Problem | Subtle forest degradation and selective logging in Madre de Dios, Peru, hidden by constant cloud cover. |
| Solution | Early Warning System based on the fusion of Radar (Sentinel-1 SAR) and Random Forest for 24/7 monitoring. |
| Deliverable | Web-based Platform (MVP) that visualizes the Subtle Degradation Map and high-impact Pitch Deck. |
🛠️ TECHNICAL STACK AND KEY METHODOLOGY
This project relies on the sequential and parallel execution of three critical components.
1. Base Data
* Source: Sentinel-1 (SLC) time series.
* Polarizations: VV and VH.
* Processing Platform: Google Earth Engine (GEE).
2. Change Detection (SAR Metric)
We used the Cumulative Sum (CuSum) algorithm on the SAR time series to generate a robust change metric, $$Rsum_{max}$$.

$$ \text{Rsum}_{\text{max}} = \max\left(\sum_{t=1}^{T} (S_t - \mu)\right) $$

* Lead: Irving (Data Engineer).
* Role: Rapid pre-processing to identify areas of potential change.
3. Classification Model (Random Forest)
A Convolutional Neural Network (CNN) model for fine-grained semantic segmentation.
* Architecture: Random Forest.
* Objective: Map the 3 classes: (1) Intact Forest, (2) Degraded Forest (Subtle), (3) Deforestation/Non-Forest.
* Success Metric: IoU for the 'Degraded Forest' class.
* Responsible: Benjamin (IA Lead/Architect).
⚙️ WORKFLOW (14-HOUR PIPELINE).

The work is organized into 3 phases with mandatory parallelization in Phase 2.

| Phase | Critical Task | Primary Role | Est. Duration |
|---|---|---|---|
| 1. Foundations and Data (0-3h) | SAR Data Pipeline in GEE (Access, Preprocessing, AOI). | Irving / Cristhian | 3h |
| 2. Modeling and Development (3-9h) | CuSum Modeling (Irving) + U-TAE Modeling (Benjamín). App Skeleton (Diego). | Parallel: Benjamín, Irving, Diego | 6h |
| 3. Integration and Pitch (9-14h) | Integration of GeoTIFFs (Maps) into the App. Finalization and Pitch Testing. | Integration: Benjamín, Irwin, Diego. Pitch: Edú | 5h |
Critical Touchpoints:
* Hour 3: Delivery of the cleaned dataset and validated AOI (Cristhian to Benjamín/Irving).
* Hour 9: Generation of the Final Degradation Map (Benjamín/Irving) and Start of Integration (Diego).

🧑‍💻 QUICK CONTACTS (Execution Roles)

| Name | Assigned Role (Hackathon) | Ask about... |
|---|---|---|
| Benjamín S. | AI Lead/Architect | U-TAE Hyperparameters, General Strategy. |
| Irving | Data Engineer/CuSum | SAR Time Series, $$Rsum_{max}$$ Output. |
| Cristhian F. | GIS/Ground Truth Expert | Data Validation, Geometries (AOI), Calibration. |
| Diego O. | Product Engineer/Backend Engineer | Integration APIs, Map Deployment. |
| Edú O. | Narrative Director | Storytelling, Pitch Script, Key Message. |


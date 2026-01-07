---
title: "Urban Thermal Environment"
collection: research
permalink: /research/thermal-environment/
---

### Motivation
Rapid urbanization in Dhaka has intensified surface thermal stress and altered vegetation dynamics. Quantifying spatiotemporal variation in land surface temperature (LST) and key spectral indices is essential for understanding urban heat patterns and environmental change.

### Goal
Assessing the spatiotemporal variation of Land Surface Temperature (LST) and Normalized Difference Vegetation Index (NDVI) of Dhaka city between 2018 and 2023 using Landsat 8 satellite imagery.

### Methodological Workflow
- Image filtering by date and cloud cover  
- Cloud masking and radiometric correction  
- Computation of NDVI
- LST derivation from TIRS bands  
- Annual aggregation and trend analysis  


<p align="center"><em>
  Comparison of land surface temperature patterns in Dhaka City between 2018 and 2023.
  <img src="/images/LST.jpg" width="80%" />
</em></p>

**The mean LST recorded was 34.72°C, with a gradual annual increase of 0.48% in comparison to 2018. Despite a decrease in LST in 2020 during COVID-19, a rising trend has been observed since 2021. The escalating LST trend is linked to factors like urban expansion, centralization, reduced vegetation cover, and waterbody alterations.**

<p align="center"><em>
  Spatiotemporal variation of NDVI from 2018 to 2023.
  <img src="/images/NDVI.jpg" width="80%" />
</em></p>


**The six-year mean NDVI stands at 0.261, indicating a low value and the prevalence of scarce vegetation in the study area. Throughout the years, the NDVI values remained notably low, with a majority of the region displaying negative NDVI values annually.**

All data processing and analysis were conducted in Google Earth Engine. The complete script is available in the repository.

📂 GEE Script: `gee/lst_indices.js`

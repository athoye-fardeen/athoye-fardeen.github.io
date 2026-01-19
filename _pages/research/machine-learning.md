---
title: "Land Surface Temperature Prediction Using Ensemble Machine Learning"
collection: research
permalink: /research/machine-learning/
---


###  Overview
Land Surface Temperature (LST) dynamics in the Dhaka Metropolitan Area were analyzed using an ensemble machine learning framework. Four regression algorithms, Random Forest (RF), AdaBoost (ADA), Histogram-based Gradient Boosting (HGB), and Extreme Gradient Boosting (XGBoost), were implemented to model the relationship between LST and remotely sensed biophysical and topographic variables. The analysis covers the period from 2020 to 2025 and enables both annual and seasonal assessments of spatio-temporal temperature patterns.

### Input Data and Features
Models were trained using satellite-derived spectral indices and elevation data from Landsat 8 and NASADEM. 
- Normalized Difference Vegetation Index (NDVI)
- Normalized Difference Built-up Index (NDBI)
- Normalized Difference Bareness Index (NDBaI)
- Elevation  

#### Correlation Heatmap
<p align="center">
  <img src="/images/feature_correlation_heatmap.png" width="50%" />
</p>

### Model Performance Evaluation

#### Quantitative Performance Metrics

| Model | Train RMSE | Train AAPRE (%) | Train R² | Train 95% CI | Test RMSE | Test AAPRE (%) | Test R² | Test 95% CI |
|------|-----------:|----------------:|---------:|-------------:|----------:|---------------:|--------:|------------:|
| Random Forest | 3.73 | 11.54 | 0.84 | 7.31 | 6.33 | 18.16 | 0.52 | 12.40 |
| AdaBoost | 6.69 | 22.58 | 0.48 | 13.09 | 6.89 | 19.84 | 0.43 | 13.50 |
| HistGradientBoosting | 6.39 | 21.24 | 0.52 | 12.53 | 6.39 | 21.24 | 0.52 | 12.53 |
| XGBoost | 6.12 | 21.24 | 0.56 | 12.00 | 6.12 | 21.24 | 0.56 | 12.00 |

**The Random Forest model shows the best overall performance, with the lowest RMSE, the lowest AAPRE, and the highest R². AdaBoost yields the weakest results, with higher errors and lower R². HistGradientBoosting and XGBoost exhibit moderate and nearly identical performance, but both underperform relative to Random Forest.**

### Diagnostic Analysis

#### Feature Importance
<p align="center"><em>
   <img src="/images/feature_importance_Random_Forest.png" width="48%" />
  <img src="/images/feature_importance_AdaBoost.png" width="48%" />
  <img src="/images/feature_importance_HistGradientBoosting.png" width="48%" />
  <img src="/images/feature_importance_XGBoost.png" width="48%" />
</em></p>

**Season is the most consistently important predictor across all models, with vegetation and built-up indices also playing key roles. Elevation has minimal influence.**

#### Observed vs Predicted LST

<p align="center"><em>
   <img src="/images/scatter_Random_Forest.png" width="48%" />
  <img src="/images/scatter_AdaBoost.png" width="48%" />
  <img src="/images/scatter_HistGradientBoosting.png" width="48%" />
  <img src="/images/scatter_XGBoost.png" width="48%" />
</em></p>

### Spatial Prediction Results

#### Seasonal LST Prediction Maps
**Summer**  
![Summer LST](assets/maps/seasonal/lst_summer.png)

**Monsoon**  
![Monsoon LST](assets/maps/seasonal/lst_monsoon.png)

**Winter**  
![Winter LST](assets/maps/seasonal/lst_winter.png)

### Annual LST Prediction Map

![Annual LST](assets/maps/annual/lst_annual.png)

### Tools
- Google Earth Engine
- Python
- ArcGIS Pro


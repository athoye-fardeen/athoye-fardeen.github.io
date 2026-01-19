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
Heatmap showing relationships among input variables and LST.

### Model Performance Evaluation

#### Quantitative Performance Metrics

| Model | Train R² | Test R² | AAPRE | CI | RMSE |
|------|----------|---------|-------|----|------|
| RF   |          |         |       |    |      |
| XGB  |          |         |       |    |      |
| HGB  |          |         |       |    |      |
| ADA  |          |         |       |    |      |


### Diagnostic Analysis

#### Feature Importance
**Random Forest**  
![RF Feature Importance](assets/figures/feature_importance/rf_feature_importance.png)

**XGBoost**  
![XGB Feature Importance](assets/figures/feature_importance/xgb_feature_importance.png)


#### Observed vs Predicted LST

**Random Forest**  
![RF Obs vs Pred](assets/figures/observed_predicted/rf_obs_pred.png)

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


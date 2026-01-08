---
title: "Spatial Heterogeneity in the Urban Heat Island–Air Pollution Nexus"
collection: research
permalink: /research/urban-heat/
---

### Problem Statement
Rapid urbanization has intensified the dual challenges of Urban Heat Islands (UHI) and air pollution in cities. While significant research has focused on the spatial and temporal characteristics of air pollution and UHI, the spatially heterogeneous relationship between them remains underexplored. This research examined how underlying air pollutants influence the characteristics of the UHI phenomenon in a Global South City, Dhaka.

### Research Questions
- Do air pollutants have the same influence on UHI intensity across different areas of a city, or do their impacts vary spatially?
- Can global regression methods, such as OLS, effectively capture localized variations in air pollution, or are more specific local models more appropriate?
- If spatial heterogeneity is present, should environmental and urban planning policies remain standardized throughout a city, or should they be adapted to reflect local conditions?

### Key Variables
- Urban Thermal Field Variance Index (UTFVI) derived from Land Surface Temperature (LST)
- PM<sub>2.5</sub> , NO<sub>2</sub> , SO<sub>2</sub> , CO, O<sub>3</sub>

<p align="center">
  <img src="/images/Getis_Ord.jpg" width="49.1%" />
  <img src="/images/MGWR.jpg" width="50%" />
</p>
<p align="center"><em>
  Left: Hotspot analysis (Getis–Ord Gi*). Right: Results estimated from Multi-scale Geographically Weighted Regression.
</em></p>

### Model Diagnostics
**Table 1.** OLS regression results.

| Variable   | Coefficient | Std. Error | t-Statistic | p-value | Robust Std. Error | Robust t | Robust p-value | VIF |
|------------|------------:|-----------:|------------:|--------:|-----------------:|---------:|---------------:|----:|
| Intercept  | -154.43 | 10.58 | -14.59 | 0.000* | 24.90 | -6.20 | 0.000* | — |
| PM₂.₅      | 0.35 | 0.04 | 8.17 | 0.000* | 0.09 | 3.91 | 0.000* | 2.90 |
| NO₂        | 0.51 | 0.06 | 8.77 | 0.000* | 0.16 | 3.26 | 0.002* | 2.90 |

*An asterisk next to a number indicates a statistically significant p-value (p < 0.01), and (**) indicates a statistically significant p-value (p<0.05)

**Table 2.** OLS model diagnostics and spatial dependence tests.

| Metric | Value |
|-------|------:|
| Dependent Variable | UTFVI |
| Multiple R² | 0.89 |
| Adjusted R² | 0.88 |
| AICc | 1044.87 |
| Joint F-Statistic | 377.02 (p < 0.001) |
| Joint Wald Statistic | 284.15 (p < 0.001) |
| Koenker (BP) Statistic | 36.00 (p < 0.001) |
| Jarque–Bera Statistic | 145.17 (p < 0.001) |
| Global Moran’s I (Residuals) | −0.054 |
| Moran’s I p-value | 0.049** |

**PM₂.₅ and NO₂ exhibit statistically significant positive associations with UTFVI, while diagnostic tests indicate heteroskedasticity and residual non-normality, justifying the use of spatial or multi-scale models.**

### MGWR–OLS Model Comparison
**Table 3.** Summary of MGWR model diagnostics and comparison with the global OLS model. ** indicates significance at p ≤ 0.05.

| Diagnostic | MGWR | OLS |
|-----------|-----:|----:|
| Residual Sum of Squares | 338,108.16 | — |
| AICc | 1031.05 | 1044.87 |
| ΔAICc (OLS − MGWR) | 13.82 | — |
| R² | 0.92 | 0.89 |
| Adjusted R² | 0.91 | 0.88 |
| Global Moran’s I (Residuals) | -0.027 | -0.054 |
| Moran’s I p-value | 0.334 | 0.049** |
| Optimal Bandwidth | 30 | — |
| Sigma-squared | 2896.38 | — |
| Sigma-squared (MLE) | 2219.47 | — |
| Effective Degrees of Freedom | 83.77 | — |

**The MGWR model substantially outperforms the global OLS model, as indicated by a lower AICc (ΔAICc = 13.82) and higher explanatory power (R² = 0.92). The non-significant Moran’s I for MGWR residuals confirms that spatial autocorrelation is effectively addressed, whereas the OLS model exhibits significant residual clustering, justifying the use of a multi-scale spatial approach.**

### Spatial Patterns of MGWR Regression Estimates
**Table 4.** Summary of MGWR explanatory variables showing spatial scale (neighbourhood size) and proportion of statistically significant local coefficients.

| Variable | Neighbours (% of Features) | Significant (% of Features) |
|---------|---------------------------:|----------------------------:|
| Intercept | 32 (34.04%) | 94 (100.00%) |
| NO₂ | 34 (36.17%) | 88 (93.62%) |
| PM₂.₅ | 32 (34.04%) | 94 (100.00%) |

*a.* The percentage of neighbours reflects the spatial scale of the relationship, ranging from local to global depending on the geographical context.

*b.* Percentages indicate the proportion of spatial features with statistically significant local coefficients.

### MGWR Coefficient Summary Statistics
**Table 5.** Summary statistics of local MGWR coefficient estimates for each explanatory variable, showing spatial heterogeneity across wards.

| Variable   | Minimum | Mean   | Maximum | Standard Deviation |
|-----------|--------:|-------:|--------:|-----------------:|
| Intercept | -209.23 | -172.87 | -135.42 | 23.63 |
| NO₂       | 0.37    | 0.63    | 0.83    | 0.14 |
| PM₂.₅     | 0.12    | 0.29    | 0.45    | 0.09 |

The MGWR coefficients indicate that PM₂.₅ and NO₂ have positive effects on UTFVI across all locations, with moderate spatial variability, while the intercept shows broader variation reflecting baseline differences in urban thermal vulnerability.

### Status
Undergraduate Thesis/Completed

### Author
Fardeen Shakur Athoye

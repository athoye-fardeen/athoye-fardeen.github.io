---
title: "Highway Conditions During Festivals in Northern Bangladesh"
collection: projects
permalink: /projects/highway-conditions/
---

## Overview
This study examines the impact of festival-related travel demand on highway conditions in the northern region of Bangladesh, utilizing real-time traffic data obtained from Google Maps. Approximately 50 million people travel across districts during the Eid festivals in Bangladesh, placing extreme pressure on the country's highway infrastructure. Despite the magnitude of this phenomenon, limited research exists on festival-induced traffic congestion in the Bangladeshi context. The study covers 16 northern regions of Bangladesh, connected to Dhaka through national highways.

## Data Collection
Traffic data were collected using the **Google Maps** platform:
- Five days before Eid (June 24–28, 2023)
- Five days after Eid (June 30–July 4, 2023)
- Four-hour intervals (8 AM–12 AM)
- Bidirectional trips between Dhaka and regional centers

## Key Variables
- Dependent Variable (Journey time)
- Independent Variable (Days leading to festival, Peak hours, Distance travelled, Number of congestion points)

## Univariate Analysis
### Table 1  Results of the univariate analysis 
##### Categorical Variables (Days leading to festival, Peak hours)

| Dependent Variable | Independent Variable | t (df) | p-value |
|-------------------|----------------------|--------|---------|
| Journey Time | Days to Festival | 16.9 (33) | 0.029** |
| Journey Time | Peak Hours | 2.4 (4) | 0.03** |

**Note:** ** indicates significance at the 95% confidence level.

##### Continuous Variables (Number of congestion points, Total distance along the best path (km) )

| Dependent Variable | Independent Variable | t (df) | p-value | r-value |
|-------------------|----------------------|--------|---------|---------|
| Journey Time | Number of Red Points | 14.433 (763) | 2.2e-16** | 0.463 |
| Journey Time | Number of Dark Red Points | 2.9851 (763) | 0.002925 | 0.107 |
| Journey Time | Total Distance (km) | 101.06 (763) | 2.2e-16** | 0.965 |

**Note:** ** indicates significance at the 95% confidence level.

#### Table 2 Model Statistics

| Statistic | Model 1: Before Eid | Model 2: After Eid |
|---------|----------------------------|----------------------------|
| F-statistic (df) | 1037 (6, 375) | 1262 (6, 375) |
| p-value | 2.2e-16 | 2.2e-16 |
| R² | 0.9431 | 0.9528 |
| Adjusted R² | 0.9422 | 0.9520 |

**Both models exhibit strong explanatory power, with adjusted R² values exceeding 0.94, indicating that the selected variables explain a substantial proportion of variation in journey time during both pre- and post-Eid periods.**

## Multivariate Analysis
**Stepwise multiple linear regression**
#### Table 3 Multivariate Analysis Results

| Variable | Model 1: Before Eid (Coefficient) | Model 1: p-value | Model 2: After Eid (Coefficient) | Model 2: p-value |
|--------|----------------------------------|------------------|----------------------------------|------------------|
| Intercept | 0.3812 | 9.07e-5*** | 0.0825 | — |
| **Peak Hours (Baseline: 11:59 AM)** |  |  |  |  |
| 8:00 AM | 0.2424 | 0.00079*** | 0.2424 | — |
| 12:00 PM | 0.7470 | — | 0.3508 | 2.74e-6*** |
| 4:00 PM | 0.1710 | — | 0.5971 | 4.67e-15*** |
| 8:00 PM | 0.2233 | 1.68e-6*** | 0.0990 | 0.00228** |
| Total Distance of Best Path (km) | 0.0218 | <2e-16*** | 0.0229 | <2e-16*** |
| Number of Red Points | 0.0208 | 9.22e-7*** | 0.0459 | — |

**Notes:**  
***Significant at 1% level  
**Significant at 5% level  
*Significant at 10% level

**The multivariate regression results indicate that travel distance and congestion intensity significantly influence journey time in both pre- and post-Eid periods. Peak-hour effects intensify after Eid, reflecting staggered return trips and increased traffic variability.**

**Diagnostic tests for linear regression assumptions**
<p align="center">
  <img src="/images/Transport-1.jpg" width="49%" />
  <img src="/images/Transport-2.jpg" width="49%" />
</p>
<p align="center"><em>
  Left: Assumption Test of Linear Regression Model for Model-1. Right: Assumption Test of Linear Regression Model for Model-2.
</em></p>

### Key Takeaways
- Journey time increased steadily before Eid, peaking one day before the holiday in several regions. Post-Eid congestion persisted due to delayed return trips and adverse weather conditions.
- Travel time increased significantly during peak hours, with the **afternoon (4 PM)** period showing the highest congestion due to synchronized departure from workplaces.
- Regression results show congestion points have a stronger impact on travel time **after Eid** than before.

### Tools
- RStudio
- QGIS

### Author
Fardeen Shakur Athoye





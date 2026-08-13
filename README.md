#  Predictive Modeling of Wheat Yield in Pakistan

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

##  Executive Summary
Predicting crop yield for a staple national commodity like wheat is vital for **food security, supply chain planning, and macroeconomic policy**. 

This project delivers a robust machine learning framework that models historical wheat yields across Pakistan using a combination of **agro-climatic, agronomic, and socio-economic datasets** spanning two decades (2000–2019). The analysis is structured around **Norman’s Action Cycle** to align human-centric data interaction with analytical problem-solving.

---

##  Key Results & Model Performance

The predictive pipeline utilizes a **Random Forest Regressor** to model non-linear interactions between weather patterns and agronomic inputs.

* **$\mathbf{R^2}$ Score:** `0.91` *(Explains 91% of national wheat yield variance)*
* **RMSE:** `0.057 t/ha` *(~2.15% relative error margin)*
* **MAE:** `0.051 t/ha` *(~1.92% relative error margin)*

---

##  Dataset Architecture & Engineering

Data from three distinct international databases was aggregated, cleaned, and feature-engineered:

| Dataset | Source | Extracted Features | Purpose / Role |
| :--- | :--- | :--- | :--- |
| **FAOSTAT** | UN FAO | Harvested Area, Production Volume, Derived Yield | **Target Variable ($y$)** |
| **NASA POWER** | NASA | Mean Temperature ($^\circ\text{C}$), Cumulative Rainfall ($\text{mm}$), Solar Radiation ($\text{MJ/m}^2/\text{day}$) | **Climatic Features ($X$)** |
| **World Bank** | World Bank Open Data | Fertilizer Consumption ($\text{kg/ha}$) | **Agronomic Input ($X$)** |

---

##  Key Insights & Feature Importance

Feature importance analysis revealed the core drivers of wheat productivity in the region:

1.  **Fertilizer Usage (~43.4% Importance):** Primary human-driven input driving soil fertility and yield potential.
2.  **Solar Radiation (~27.8% Importance):** Crucial during the grain-filling stage for optimal photosynthesis.
3.  **Temperature (~17.3% Importance):** Heat stress during critical growing months negatively impacts output.
4.  **Precipitation (~11.5% Importance):** Moderate impact due to heavy reliance on canal irrigation infrastructure.

---

##  Methodology: Norman’s Action Cycle

The project execution strictly followed Norman's 7-Stage Framework:
1. **Goal Formation:** Establish baseline target for national wheat yield predictions.
2. **Intention:** Combine environmental and economic variables to anticipate yield shifts.
3. **Action Specification:** Extract, align, and clean 20 years of multi-source time-series data.
4. **Action Execution:** Aggregated daily climate parameters into seasonal indicators; merged datasets on `Year`.
5. **Perception:** Visualized yield trends against extreme heatwaves and fertilizer subsidy cycles.
6. **Interpretation:** Evaluated non-linear interactions using Random Forest feature importances.
7. **Evaluation:** Validated model stability against standard regression evaluation metrics ($R^2$, $RMSE$, $MAE$).

---

##  Getting Started

### 1. Prerequisites
Ensure you have Python installed:
```bash
python --version  # Recommended: Python 3.9+

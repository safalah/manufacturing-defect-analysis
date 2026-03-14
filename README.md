# EV Battery Quality Control Analysis

## Overview

This repository contains a comprehensive data analysis of the manufacturing quality control (QC) process for Electric Vehicle (EV) batteries. By leveraging synthetic defect data from 20,000 battery cells, the project identifies key drivers of failure (Scrap), explores environmental impacts on performance, and provides actionable recommendations to improve manufacturing yield and consistency.

## Dataset Description

The analysis is based on a dataset of **20,000 battery cell records**, featuring:

- **Manufacturing Context:** Production Line (1-3), Shift (Morning, Evening, Night), and Supplier (ChemCorp, LithioMat, VoltIndustries).
- **Environmental Factors:** Ambient Temperature (°C).
- **Physical Parameters:** Anode Overhang (mm) and Electrolyte Volume (ml).
- **Performance Metrics:** Internal Resistance (mOhm), Capacity (mAh), and 50-Cycle Retention (%).
- **Quality Metrics:** Defect Type, Inspector Comments, and QC Grade (Grade A, Grade B, Scrap).

## Key Findings

- **Quality Distribution:** ~66% of batteries achieve Grade A, while 15% are classified as Scrap.
- **Root Cause Chain:**
  1. **Ambient Temperature** affects **Electrolyte Volume** (likely due to evaporation).
  2. Low Electrolyte Volume increases **Internal Resistance**.
  3. High Internal Resistance directly degrades **Capacity** and **Retention**.
- **Supplier Performance:** VoltIndustries shows a significantly higher scrap rate (~18.7%) compared to other suppliers.
- **Tool Wear:** Analysis of Anode Overhang indicates gradual tool wear over time, leading to alignment defects.

## Technical Stack

The analysis was performed using **Python** and the following libraries:

- **Data Manipulation:** `pandas`, `numpy`
- **Visualization:** `matplotlib`, `seaborn`
- **Network Analysis:** `networkx`
- **Machine Learning:** `scikit-learn` (RandomForest for Feature Importance)
- **Statistical Analysis:** `scipy`

## Methodology

1. **Exploratory Data Analysis (EDA):** Identifying correlations between environmental factors and battery performance.
2. **Root Cause Analysis:** Mapping the causal relationship between manufacturing parameters and final QC grades.
3. **Feature Importance:** Using Random Forest to identify the most critical predictors of battery quality.
4. **NLP Insights:** Analyzing inspector comments to identify recurring mechanical issues like "recalibrated," "vibration," and "spill."

## Recommendations

- **Climate Control:** Stabilize factory temperature at electrolyte filling stations.
- **Supplier Audit:** Conduct a quality audit for VoltIndustries components.
- **Predictive Maintenance:** Use Anode Overhang drift data to schedule tool maintenance proactively.
- **Automated Gate-keeping:** Implement early-stage QC flags based on Internal Resistance thresholds.

## Repository Structure

- `ev_battery_qc_analysis.ipynb`: Detailed Jupyter Notebook with all data processing, visualizations, and modeling.
- `ev_battery_qc_analysis_report.md`: A structured summary report of the analysis and findings.
- `ev_battery_qc_dataset.csv`: The source dataset used for this analysis.
- `Dataset link.url`: Link to the original dataset source.

---

_Developed as part of an EV Battery Manufacturing Quality Control initiative._

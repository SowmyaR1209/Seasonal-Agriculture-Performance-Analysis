# Seasonal Agriculture Performance Analysis

A data analytics project analyzing how agricultural performance — yield, resource usage, environmental conditions, and economic outcomes — varies across the **Kharif**, **Rabi**, and **Zaid** seasons in India.

> VOIS AICTE Batch 1, 2026–2027 — Major Project

## Overview

Agricultural performance is shaped by seasonal variation in rainfall, temperature, resource availability, and market conditions. This project analyzes a farm-level dataset to uncover meaningful seasonal patterns, trends, and relationships, and translates them into evidence-based recommendations for farmers, policymakers, and agri-businesses.

## Dataset

- **4,000 farm-level records**
- **8 states**, **8 crops**, **3 seasons** (Kharif, Rabi, Zaid), **4 irrigation methods**
- Fields span four categories:
  - **Environmental**: rainfall, temperature, humidity, sunlight hours, soil pH, soil moisture
  - **Resources**: fertilizer, pesticide, irrigation method, water used, seed quality
  - **Output**: yield, production, water efficiency, disease/pest risk
  - **Economic**: market price, total cost, revenue, profit

## What This Project Does

1. **Data cleaning** — imputes missing values (season/crop-aware median), checks for duplicates, and caps outliers using the IQR method
2. **Exploratory analysis** — compares environmental conditions, resource usage, yield, and economic performance across seasons using boxplots, bar charts, and violin plots
3. **Relationship analysis** — correlation heatmap and scatterplots to identify what actually drives yield and profit
4. **Cross-analysis** — Crop × Season and State × Season pivot heatmaps
5. **Statistical testing** — one-way ANOVA to confirm which seasonal differences are statistically significant, not just visual
6. **Insights & recommendations** — evidence-based conclusions for each stakeholder group

## Key Findings

- **Yield** is highest in Kharif (5.50 t/ha) vs Zaid (4.64 t/ha), but the difference is **not** statistically significant (ANOVA p = 0.31)
- **Profit**, however, differs significantly by season (p ≈ 2.3e-15) — Zaid runs an average **net loss** (-₹23,235), driven by low rainfall and the lowest revenue of the three seasons
- **Water efficiency** (r = 0.93) is a far stronger yield driver than fertilizer/nutrient input (r ≈ 0.05) — a key actionable insight
- **Disease/pest risk** is highest in Kharif (54.5%), consistent with its high rainfall and humidity
- Regional performance can swing sharply by season — e.g. Gujarat is the top-profit state in Kharif but one of the worst in Zaid

Full findings and supporting charts are in the notebook and project presentation.

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3 |
| Environment | Jupyter Notebook |
| Data handling | pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Statistical testing | SciPy (one-way ANOVA) |

## Repository Structure

├── Seasonal_Agriculture_Performance_Analysis.ipynb # Full analysis notebook
├── seasonal_agriculture_performance_dataset.csv # Dataset
├── Seasonal_Agriculture_Performance_Analysis_PPT.pptx # Project presentation
└── README.md


## How to Run

1. Clone the repository:
```bash
   git clone <your-repo-url>
   cd <repo-folder>
```
2. Install dependencies:
```bash
   pip install pandas numpy matplotlib seaborn scipy
```
3. Launch Jupyter and open the notebook:
```bash
   jupyter notebook Seasonal_Agriculture_Performance_Analysis.ipynb
```
4. Run all cells in order (Cell → Run All).

## Future Scope

- Multi-year seasonal trend analysis to test whether current patterns are structural or specific to one year
- District- and micro-climate-level granularity to explain state-level variation
- Predictive modeling (regression/ML) for yield and profit forecasting
- Interactive dashboard (e.g. Power BI / Streamlit) for real-time seasonal monitoring
- Integration with live weather and market-price APIs

## Author

**Sowmya R**

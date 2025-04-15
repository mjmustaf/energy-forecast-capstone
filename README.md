# Capstone Project: Predicting Solar Energy Output

## Overview
A machine learning model to predict daily solar energy output based on economic and demographic data such as GDP, population, and GDP per capita. The goal is to help energy providers and policymakers anticipate production levels and plan accordingly.

## Research Question
How accurately can solar energy output be predicted using GDP, population, and GDP per capita?

## Dataset
- Primary: [World Energy Consumption – Kaggle](https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption/data)
- Variables: solar consumption (target), GDP, population, GDP per capita (features)
- Records: ~22,000 (cleaned to ~1,000 for solar-relevant data)

## Methodology
- Cleaned missing and duplicate values
- Feature engineering: solar per million population, GDP per capita, decade buckets
- Exploratory analysis: visualized consumption growth trends and variable relationships
- Modeled with Linear Regression as a baseline

## Results
- **Baseline Model**: Linear Regression
- **RMSE**: 39.41
- **R² Score**: -1.27
- Conclusion: Limited predictive power from economic indicators alone and solar growth is non-linear and driven by external factors

## Next Steps
- Introduce weather and sunlight data to improve prediction accuracy
- Explore advanced models like Random Forest and XGBoost
- Normalize skewed features


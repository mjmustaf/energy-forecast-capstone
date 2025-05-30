# Predicting Solar Energy Output Using Machine Learning

---

##  Project Overview

As the world shifts toward sustainable energy, solar power is one of the fastest-growing contributors to global electricity generation. However, the variability of solar energy—driven by economics, geography, and environmental factors—makes it difficult to plan for consistent supply.

This capstone project explores the question:  
**Can we forecast a country's solar energy output using only publicly available economic indicators like GDP and population?**

---

##  Business Context

Energy providers, grid operators, and governments need reliable forecasts to:
- Balance supply and demand
- Optimize energy storage
- Plan infrastructure investments
- Reduce reliance on fossil fuels

Accurate forecasting enables smarter decision-making, and while environmental data (sunlight hours, temperature) is ideal, we wanted to explore how far we can go with just macro-level indicators.

---

##  Dataset Details

- **Source**: [World Energy Consumption Dataset (Kaggle)](https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption/data)
- **Scope**: ~22,000 country-year records, 129 columns
- **Features Used**: GDP, population, solar consumption, derived features
- **Target Variable**: `solar_consumption` (in TWh)

---

##  Methodology

**1. Data Cleaning**
- Removed columns with >50% missing data
- Filtered for rows with valid GDP, population, and solar energy output

**2. Feature Engineering**
- Created `solar_per_million`, `gdp_per_capita`, and `decade` buckets

**3. Exploratory Data Analysis**
- Visualized solar energy trends over time
- Analyzed distribution of consumption and feature correlations

**4. Modeling and Evaluation**
- Baseline: Linear Regression
- Advanced Models: Random Forest, XGBoost, K-Nearest Neighbors
- Performance evaluated using RMSE and R² metrics

---
##  Model Comparison Summary

| Model                | RMSE  | R² Score |
|----------------------|-------|----------|
| Linear Regression     | 39.41 | -1.27     |
| Random Forest         | 9.00  | 0.88      |
| XGBoost               | 9.92  | 0.86      |
| K-Nearest Neighbors   | 14.04 | 0.72      |


###  Observations
- **Random Forest** performed best with the lowest RMSE and highest R².
- **XGBoost** also achieved strong results.
- **KNN** was simpler but less accurate.
- **Linear Regression** underperformed, confirming the data relationships are non-linear.


---

##  Project Structure

```
energy-forecast-capstone/
├── data/
│   └── World Energy Consumption.csv
├── notebooks/
│   ├── 01_eda_and_linear_model.ipynb
│   ├── 02_random_forest_model.ipynb
│   ├── 03_xgboost_model.ipynb
│   ├── 04_knn_model.ipynb
│   └── 05_model_comparison_summary.ipynb
├── presentation/
├── README.md
├── .gitignore
```

---

##  How to Run

1. Clone this repository  
2. Open any of the notebooks inside the `notebooks/` folder  
3. Ensure the dataset is placed in the `data/` folder  
4. Run the notebook(s) top to bottom in Jupyter or VSCode  

---

##  Limitations

- No weather data (sunlight, temperature, cloud cover)
- Many countries had near-zero solar output until mid-2010s
- Economic indicators alone are too broad for precise modeling

---

##  Potential Enhancements

- Integrate weather and climate data through APIs (e.g., OpenWeatherMap)
- Use deep learning models for time-series forecasting
- Add geospatial features (latitude, elevation, climate zones)
- Deploy an interactive dashboard or forecasting API

---

This project was completed as part of an AI/ML capstone program. It lays the foundation for future work in sustainable energy forecasting using machine learning.

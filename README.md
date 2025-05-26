# Predicting Solar Energy Output Using Machine Learning

## Business Understanding

As nations increasingly shift to renewable energy, solar power has become a critical contributor to clean electricity. However, solar energy generation is inherently variable and influenced by economic, technological, and geographic factors. Accurately forecasting solar energy output is crucial for energy providers, policymakers, and urban planners to make informed decisions about infrastructure investments, storage capacity, and grid stability.

This project addresses the challenge: **Can we predict solar energy output using publicly available economic and demographic data such as GDP, population, and energy policies?**

## Dataset Overview

- Source: [World Energy Consumption – Kaggle](https://www.kaggle.com/datasets/pralabhpoudel/world-energy-consumption/data)
- Records: 22,000+ country-year observations
- Features: Over 100 columns covering fossil, renewable, and nuclear energy consumption; population; GDP; and emissions.
- Target: Solar consumption (TWh) per country per year

## Methodology

The workflow includes:

1. **Data Cleaning**: Removed columns with >50% missing values, filtered out rows lacking solar and GDP data.
2. **Feature Engineering**:
   - Created solar output per million people
   - Calculated GDP per capita
   - Extracted decade for time-grouping
3. **EDA**: Conducted visual and statistical analysis to detect trends and relationships.
4. **Modeling**:
   - Baseline model using Linear Regression
   - Evaluated with RMSE and R² metrics

## Results and Key Findings

- **RMSE**: 39.41
- **R² Score**: -1.27

These results indicate that the model failed to generalize well. The poor R² suggests that economic indicators alone are insufficient to explain solar output variability, which is likely more dependent on climate, technology adoption, and national policies.

## Visualizations

Visualizations included:
- Histograms of solar energy output
- Line plots showing growth in solar consumption over time
- Correlation heatmaps identifying relationships between GDP, population, and energy features

## Limitations

- No weather or geographic data (e.g., sunlight hours, elevation)
- High sparsity in early years for solar data
- Limited features related to energy policy or technological infrastructure
- Linear model unable to capture non-linear growth in solar adoption

## Recommendations

To improve prediction accuracy:
- Integrate weather and solar irradiance data via external APIs
- Include policy or investment indicators (e.g., subsidy data)
- Apply advanced models such as Random Forest, XGBoost, or neural networks
- Deploy a dashboard for visual scenario analysis

## How to Run the Code

1. Clone the GitHub repository
2. Navigate to the `notebooks/` folder
3. Open and run `01_eda_modeling.ipynb` in Jupyter or Colab
4. Ensure the dataset `World Energy Consumption.csv` is placed in the `data/` folder

---

*This report is submitted as part of a capstone project for an AI/ML certification program.*

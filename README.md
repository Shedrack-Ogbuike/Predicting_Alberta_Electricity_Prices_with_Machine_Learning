# Predicting Alberta’s Electricity Prices with Machine Learning

This project uses machine learning to predict average electricity prices in Alberta based on historical electricity generation, market, and environmental data.

## Project Overview
The goal is to build predictive models for electricity prices and evaluate their performance. The dataset includes power generation data from various sources, market information, and additional environmental features.

## Data Preparation
- Dataset: `Clean Data.csv`
- Target variable: `Avg. Price`
- Dropped timestamps and redundant columns to avoid double counting.
- Filled missing values (e.g., coal generation set to 0 as it is no longer used).
- Final dataset contains 26,304 rows × 46 features.

## Feature Scaling
- Linear models use StandardScaler to normalize features.
- Non-linear models (Random Forest) do not require scaling.

## Models Implemented

### Linear Regression
- Baseline linear model.
- **Training R²:** 0.49  
- **Validation R²:** 0.50  
- Linear model performance is limited due to non-linear relationships in the data.

### Ridge Regression
- Linear model with L2 regularization.
- **Best alpha:** 0.01  
- **Training R²:** 0.49  
- **Validation R²:** 0.50  
- Slight improvement over simple linear regression, still limited.

### Random Forest Regressor
- Non-linear tree-based model.
- Initial performance: **Training R² ≈ 0.98**, **Validation R² ≈ 0.86**
- Hyperparameter tuning slightly improved results.
- Captures non-linear relationships effectively.
- Provides feature importance for model interpretation.

## Results
- Predictions closely match actual prices.  
- **Average Predicted Price:** 120.70  
- **Average Actual Price:** 120.16  
- Residuals analysis shows minimal bias.  
- Top features influencing prices are identified via Random Forest feature importances.

## Key Takeaways
- Linear models are insufficient due to non-linear data patterns.  
- Random Forest provides strong predictive performance.  
- Feature importance analysis helps understand key drivers of electricity prices.  
- The model can be used for forecasting and decision-making in electricity markets.

## Visualization
- Scatter plots of Actual vs Predicted prices.  
- Residuals vs Predicted values.  
- Bar plots of top 15 feature importances.  

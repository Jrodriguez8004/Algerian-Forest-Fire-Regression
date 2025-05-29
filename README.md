# Algerian Forest Fire Regression

## Project Overview

This project analyzes the Algerian Forest Fire dataset to predict the Fire Weather Index (FWI), an important indicator for assessing fire risk in forests. Using meteorological and fire index variables, various regression models were developed and evaluated.

## Dataset

The dataset contains meteorological measurements and fire indices collected over several days and regions in Algeria. The target variable is the Fire Weather Index (FWI).

## Features Used

- Day
- Temperature
- Relative Humidity (RH)
- Rain
- Fine Fuel Moisture Code (FFMC)
- Duff Moisture Code (DMC)
- Drought Code (DC)
- Initial Spread Index (ISI)
- Build Up Index (BUI)

## Methods

- Data cleaning and preprocessing (no missing values found)
- Exploratory data analysis with visualizations to understand feature relationships
- Model building using:
  - Linear Regression
  - Ridge Regression (L2 regularization)
  - Lasso Regression (L1 regularization)
- Hyperparameter tuning via cross-validation for Ridge and Lasso regression
- Model evaluation using RMSE, MAE, and R² metrics
- Saving the best performing model (Ridge Regression) as a pickle file

## Results

- Ridge regression with optimized alpha showed the best performance with an R² score of approximately 0.98 on test data.
- Visualizations revealed significant correlations between FWI and the selected features, justifying their inclusion in the models.

## Usage

1. Run the Jupyter notebook `Algerian_Forest_Fire_Analysis.ipynb` to reproduce the analysis.
2. The trained Ridge regression model is saved as `best_model.pkl` and can be loaded to make predictions on new data.

```python
import pickle

with open('best_model.pkl', 'rb') as f:
    model = pickle.load(f)

# Example prediction
# predictions = model.predict(new_data)

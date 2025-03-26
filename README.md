# US Total Housing Starts ML Forecasting Project

This project applies machine learning and time series modeling techniques to forecast monthly US Total Housing Starts using a set of macroeconomic, freight, and housing market indicators. The goal is to create a transparent and interpretable forecasting pipeline with real-world applicability.

## Objective
To develop an end-to-end machine learning pipeline that predicts monthly US Total Housing Starts by incorporating a diverse set of economic indicators. The project handles challenges such as data frequency mismatch, interpolation, lagged effects, and model selection.

## Features Used
The model incorporates the following variables:

- Household Estimates (Linear Regression)
- PPI for Deep Sea Freight (ARIMA)
- PPI for Truckload Freight (Random Forest with lag features)
- Real GDP per Capita (Theil-Sen Regression)
- Zillow Observed Rent Index (ZORI) (Linear Regression)
- Median Multiple (Calculated using):
  - Median Household Income (Linear Regression)
  - Median House Prices (Holt-Winters Exponential Smoothing)
- Mortgage Spread over 10-Year Treasury (SARIMA with Box-Cox transformation)

## Methodology

1. Data Preprocessing
   - Aggregated and aligned time series of different frequencies (monthly, quarterly, annual).
   - Applied interpolation and extrapolation to fill gaps and extend predictors to the forecast horizon.

2. Feature Engineering
   - Used lags and transformations to capture temporal dependencies and economic dynamics.
   - Ensured stationarity and handled seasonality where applicable.

3. Modeling Approach
   - Combined regression and time series forecasting models per feature.
   - Final forecast derived using ensemble predictions from extrapolated drivers.

4. Validation
   - Out-of-sample validation using rolling/expanding windows.
   - Visual and statistical evaluation of residuals.

## Evaluation Metrics

- Root Mean Squared Error (RMSE)  
- Mean Absolute Error (MAE)  
- Directional Accuracy  
- Plot-based inspection (see below)

## Sample Forecast Output

In the report written 

> Replace the above with your actual chart export from matplotlib.

## Tools & Libraries
- Python (pandas, numpy, scikit-learn, statsmodels)
- Time Series Forecasting: ARIMA, SARIMA, Holt-Winters, Theil-Sen
- ML Models: Linear Regression, Random Forest
- Visualization: matplotlib, seaborn
- Environment: Jupyter Notebook

## Learning Outcomes
- Learned to integrate multi-source economic data with different frequencies and granularities.
- Applied advanced regression and forecasting models tailored to each variable's properties.
- Practiced explainable ML in a macroeconomic forecasting context.
- Improved skills in model validation, forecasting logic, and time series diagnostics.

## Possible Extensions
- Add neural networks for sequence modeling (e.g., LSTM, Transformer)
- Expand to regional housing starts
- Incorporate policy-based features (e.g., interest rate announcements)

## Author

Benjamin Wong (@wongbenjamin25)  
Bachelor of Science (Hons.) in Data Science & Quantitative Finance  
National University of Singapore

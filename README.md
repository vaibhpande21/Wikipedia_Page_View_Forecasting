# AdEase - Time Series Forecasting for Ad Optimization

## Project Overview

AdEase is a digital advertising infrastructure that helps businesses maximize their ad reach at minimal cost. This project focuses on analyzing and forecasting page views of Wikipedia articles over 550 days to optimize ad placement for clients across different regions and languages. By leveraging time series forecasting techniques, we aim to predict future page views and enhance ad targeting strategies.

## Objective

- Analyze Wikipedia page view trends to identify high-traffic periods.
- Forecast future page views to optimize ad placement.
- Utilize exogenous campaign data to improve model accuracy for English pages.

## Data Preprocessing

### Dataset Details

1. **train_1.csv**: Contains Wikipedia article names and their daily view counts over 550 days.
   - Format: `PAGE_NAME_LANGUAGE.wikipedia.org_ACCESS_TYPE_ACCESS_ORIGIN`
   - Includes information on language, device type, and request origin (browser/spider).

2. **Exog_Campaign_eng.csv**: Indicates days with ad campaigns or major events affecting traffic (1 for campaign days, 0 otherwise).

### Data Handling Steps

- Convert date columns to a standard time series format.
- Extract relevant features from page names (language, access type, origin).
- Handle missing values using interpolation techniques.
- Normalize page views for better model performance.

## Models Used

1. **ARIMA (AutoRegressive Integrated Moving Average)**
2. **SARIMA (Seasonal ARIMA)**
3. **Facebook Prophet**

## Model Evaluation

The models are evaluated using the following metrics:

- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Percentage Error (MAPE)**

## Steps

### Data Preprocessing

1. Load dataset and parse dates correctly.
2. Extract time-based features (day, month, weekday, seasonality).
3. Handle missing values and smooth out anomalies.

### Model Building

1. Train and evaluate multiple time series models.
2. Incorporate exogenous campaign data for English pages.

### Model Evaluation

1. Compare model performance using RMSE and, MAPE scores.
2. Visualize predictions vs. actual values for insights.

## Results

- **Best-performing model**: SARIMAX achieved the lowest RMSE, MAPE and MAE.
- **Business Impact**: Predicted page view trends allow targeted ad placements, maximizing client ROI.

## Business Insights and Recommendations

1. **Optimize Ad Placement by Traffic Trends**
   - Insight: High-traffic periods vary by language and access type.
   - Recommendation: Schedule ads during peak hours for each region/language.

2. **Leverage Campaign Data for Better Performance**
   - Insight: Campaign days significantly impact page views.
   - Recommendation: Adjust ad spending dynamically on campaign days.

3. **Device-Specific Targeting**
   - Insight: Mobile access shows higher engagement than desktop in some languages.
   - Recommendation: Prioritize mobile-friendly ads for such markets.

4. **Refine Strategy for Low-Traffic Periods**
   - Insight: Some pages exhibit strong seasonality effects.
   - Recommendation: Reduce ad spending in low-traffic months and reinvest during peaks.

## Dependencies

- Python 3.x
- Pandas
- Numpy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels
- Facebook Prophet

## Acknowledgments

This project utilizes Wikipedia page view data to enhance digital ad optimization strategies. Special thanks to open-source libraries enabling advanced time series forecasting.

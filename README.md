# Tsunami Data Analysis
## Introduction
### This project involves the analysis of a dataset containing information on tsunamis, including their causes, magnitudes, intensities, and other relevant attributes. The goal is to uncover meaningful patterns and relationships in the data through various statistical analyses and modeling techniques.

## Dataset Description
The dataset consists of the following columns:

- ID
- YEAR
- MONTH
- DAY
- HOUR
- MINUTE
- LATITUDE
- LONGITUDE
- LOCATION_NAME
- COUNTRY
- REGION
- CAUSE
- EVENT_VALIDITY
- EQ_MAGNITUDE
- EQ_DEPTH
- TS_INTENSITY
- DAMAGE_TOTAL_DESCRIPTION
- HOUSES_TOTAL_DESCRIPTION
- DEATHS_TOTAL_DESCRIPTION
- URL
- COMMENTS
- MAGNITUDE_CAT

# Key Findings

## Insights from Visualizations and Analytics

### 1. Total Damage vs. Tsunamis: Most tsunamis result in limited damage (less than $1 million). Fewer tsunamis cause severe and extreme damage.

### 2. House Damage vs. Tsunamis: Most tsunamis cause damage to a limited number of houses (1 to 50). Significantly fewer events cause extensive damage to houses (more than 1000 houses).

### 3. Deaths vs. Tsunamis: Most tsunamis result in a relatively small number of deaths (1 to 50). High death tolls (over 1000 deaths) are rare.

### 4. ANOVA: Tsunami Intensity by Earthquake Magnitude Category: Higher earthquake magnitude categories tend to have higher tsunami intensities, indicating a strong relationship between earthquake magnitude and tsunami intensity.

### 5. Tsunami Counts Over Time: The number of tsunamis per year fluctuates, with periods of higher activity, particularly around the mid-20th century.

### 6. Rolling Mean & Standard Deviation: The mean number of tsunamis per year has varied over time, with noticeable increases during certain periods. The standard deviation also fluctuates, indicating varying levels of volatility in tsunami occurrences.

### 7. Differenced Time Series: Differencing helped remove trends and seasonality, making the time series more stationary.

### 8. Decomposition of Time Series: The trend component showed long-term changes in tsunami frequency, while the seasonality component indicated recurring patterns within each year.

### 9. Autocorrelation and Partial Autocorrelation: Significant lags in the data were observed, which can be useful for building time series forecasting models.

### 10. SARIMAX Model Forecast: The model indicated a slight increase in the number of tsunamis in the forecasted period, but with wide confidence intervals, suggesting considerable uncertainty in the predictions.

### 11. Forecasting
## Using a SARIMAX model, we forecasted the number of tsunamis for future years. The model indicated a slight increase in tsunami occurrences, but the confidence intervals were wide, suggesting considerable uncertainty in the forecasts.


# Analyses Conducted

# 1. Chi-Square Test
A chi-square test was conducted to check the independence between 'MAGNITUDE_CAT' and 'REGION'.

![image](https://github.com/mhdfaizjabir/Tsunami-Analysis-Forecasting/assets/91936520/34c6ab9a-d28d-4607-9dfd-3d658e31b29b)


## Interpretation for Chi-Square Test Output
Chi-Square Statistic: 159.10514397205336
P-value: 2.8705456287588696e-10
The p-value is extremely low (much less than 0.05), which indicates that there is a statistically significant association between 'MAGNITUDE_CAT' and 'REGION'. This means that the distribution of tsunami magnitude categories is not independent of the regions in which they occur.

# 2. Linear Regression
A linear regression model was built to analyze the relationship between tsunami intensity and earthquake magnitude.

![image](https://github.com/mhdfaizjabir/Tsunami-Analysis-Forecasting/assets/91936520/d1aa797c-1630-48fc-8ea8-07e61412adc6)

## Interpretation for the Linear Regression Output
R-squared: 0.005 (Indicates very little of the variability in tsunami intensity is explained by the model)
EQ_MAGNITUDE: 0.1381 (Statistically significant predictor of tsunami intensity, p-value: 0.001)

# 3. Ordinary Least Squares (OLS) Regression
An OLS regression model was used to explore the relationship between tsunami intensity and multiple predictors.

![image](https://github.com/mhdfaizjabir/Tsunami-Analysis-Forecasting/assets/91936520/a40567b9-3043-47f6-bdf1-ac99a711ed2f)

## Interpretation
R-squared: 0.005 (Indicates very little of the variability in tsunami intensity is explained by the model)
EQ_MAGNITUDE: 0.1422 (Statistically significant predictor of tsunami intensity, p-value: 0.001)
EQ_DEPTH: -0.0011 (Not a statistically significant predictor of tsunami intensity, p-value: 0.283)

# Key Findings

* Chi-Square Test: The chi-square test indicates a significant association between 'MAGNITUDE_CAT' and 'REGION', suggesting that tsunami magnitudes vary across different regions.
* Linear Regression: While earthquake magnitude is a statistically significant predictor of tsunami intensity, the model explains only a small fraction of the variance in tsunami intensity.
* OLS Regression: Similar to the linear regression, earthquake magnitude is a statistically significant predictor, but earthquake depth is not. The model explains only a small fraction of the variance in tsunami intensity.

# Conclusion
## The analyses conducted provided valuable insights into the relationship between earthquake characteristics and tsunami intensity. The visualizations highlighted key trends and patterns in the data, while the statistical models helped quantify these relationships. Despite the low explanatory power of the models, the findings underscore the importance of considering multiple factors when assessing tsunami risks.

Do checkout 
               - KAGGLE : https://www.kaggle.com/code/mohammadfaizjabir/tsunami-data-analysis-and-forcasting
               - BLOG  : https://faiztech.hashnode.dev
               - LINKED IN : https://www.linkedin.com/in/mohammad-faiz-jabir/

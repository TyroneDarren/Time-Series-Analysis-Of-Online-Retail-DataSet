


# Walmart Retail Sales Forecasting & Time Series Analysis

##  Project Overview

This project presents a comprehensive time series analysis and forecasting study of Walmart store sales using Python. The objective was to explore historical revenue patterns, identify seasonal behavior, and develop a statistically robust forecasting model suitable for retail demand planning and business decision-making.

The dataset contains 33 months of sales observations (February 2010 – October 2012), enabling analysis of trend stability, seasonal dynamics, and short-term revenue forecasting.

---

## Objectives

* Structure and preprocess time-indexed retail sales data
* Analyze monthly trends and seasonal patterns
* Visualize store-level performance differences
* Build and evaluate forecasting models
* Quantify forecast accuracy using statistical metrics
* Derive business recommendations from model findings

---

##  Dataset Description

The dataset includes:

* Store-level weekly sales
* Date information
* Sales figures per store

Data was aggregated to monthly frequency using month-end resampling to better capture long-term seasonal behavior.

---

## **1.** Exploratory Data Analysis

###  Trend Analysis

Monthly sales remain relatively stable over time with no strong long-term upward or downward growth trend. Baseline monthly revenue averages approximately:

> **≈ 205 million**

---

### **2️.** Seasonality Analysis

Strong yearly seasonality is observed:

* December sales peak approximately **40% above average**
* January shows a significant post-holiday dip
* Recurring cyclical patterns confirm retail-driven demand shifts

Heatmap visualizations further confirm consistent seasonal effects across stores.

---

## **3.** Forecasting Methodology

### Model Used:

**SARIMAX (1,1,1)(0,1,1,12) with holiday regressors**

### Why SARIMAX?

* Captures autoregressive dynamics
* Models 12-month seasonal repetition
* Incorporates holiday indicators (Nov, Dec, Jan)
* Produces confidence intervals
* Handles non-stationary retail time series

A log transformation was applied to stabilize variance and ensure positive forecasts.

---

## **4.** Model Evaluation

Forecast performance was evaluated using the last 6 months as a test set.

### Accuracy Metrics:

* **MAE:** 39,488,619
* **RMSE:** 44,512,955

Relative to average monthly sales:

> Forecast error ≈ **19–22%**

Given the limited dataset (33 months) and absence of promotional or macroeconomic variables, this represents reasonable predictive performance.

---

## **5.** Key Insights

* Sales performance is stable but heavily seasonal.
* Revenue spikes are driven by predictable holiday demand.
* Forecast uncertainty increases over longer horizons.
* Extreme peaks are slightly smoothed by the model.

---

## **6.** Business Recommendations

1. **Pre-Holiday Inventory Scaling**
   Increase inventory and staffing in Q3 ahead of December peak demand.

2. **Post-Holiday Cost Control**
   Reduce operational intensity in January to manage demand contraction.

3. **Model Improvement Strategy**
   Incorporate exogenous variables such as promotions, fuel prices, and macroeconomic indicators to reduce forecast error.

4. **Rolling Retraining Implementation**
   Update forecasts monthly using recent data to adapt to behavioral shifts.

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Statsmodels (SARIMAX)

---




## 🚀 Skills Demonstrated

* Time series preprocessing
* Seasonal decomposition
* SARIMAX modeling
* Feature engineering (holiday regressors)
* Forecast validation (MAE & RMSE)
* Business interpretation of statistical models
* Visualization and communication of insights

---






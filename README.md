# forecasting_project
# TÜİK Forecasting Project: Total Turnover Index

## 1. Project Overview
This project provides a comprehensive time series forecasting analysis of the **Total Turnover Index** in Turkey. Using historical data directly from the TÜİK Data Portal, we evaluate various quantitative models to forecast the index value for the next month.

## 2. Data Source and TÜİK Connection
Data were accessed directly from the TÜİK Data Portal using the `tuikr` R package.
- **TÜİK Data Set Name:** Short-Term Economic Indicators - Turnover Indices
- **TÜİK Theme:** Theme 9 (Short-Term Business Statistics)
- **TÜİK Table Name:** Turnover Indices
- **tuikr Dataflow ID:** sts_trnv_m
- **Selected Variable:** Total Turnover Index
- **Data Frequency:** Monthly
- **Latest available observation:** [Örn: March 2026]
- **Forecast Target Period:** [Örn: April 2026]
- **Date of data access:** June 2, 2026

## 3. Research Objective
The goal is to forecast the Total Turnover Index, a key indicator for monitoring short-term economic momentum in Turkey. Accurate forecasting helps in understanding structural growth trends.

## 4. Use of TÜİK Data in R
The data was imported using the `tuikr` package. Due to temporary SDMX API connectivity issues, a reproducible `httr::GET` method via URL was utilized (approved by instructor). All data cleaning, formatting, and time series structuring were performed exclusively within the R environment.

## 5. Exploratory Time Series Analysis
The series exhibits a strong, persistent upward trend. Seasonality is also present, reflecting recurring annual economic cycles. No missing observations were detected in the final series.

## 6. Forecasting Methods Applied
The following methods were implemented: Naïve, Simple Moving Average, Weighted Moving Average, Exponential Smoothing, Holt's Linear Trend, Linear Trend Projection, Holt-Winters Multiplicative Decomposition, and Regression with Dummy Variables.

## 7. Forecast Accuracy Comparison
The candidate models were evaluated based on Bias, MAD, MSE, MAPE, RSFE, and Tracking Signal. A summary comparison table is available in `outputs/tables/accuracy_comparison.csv`.

## 8. Selection of the Superior Method
The **Holt-Winters Multiplicative Method** was selected as the superior model. It successfully captures both the trend and the expanding seasonal variations, outperforming simpler models in both MAPE and MAD metrics.

## 9. Final Next-Period Forecast
- **Selected superior method:** Holt-Winters Multiplicative
- **Forecast target period:** [Örn: April 2026]
- **Forecasted value:** [Örn: 1550.25]

## 10. Interpretation of Results
The selected model suggests continued growth in the index, consistent with the observed long-term trend. The forecast for the next period remains robust, provided economic conditions remain stable.

## 11. Limitations
The model may be sensitive to sudden structural breaks or revisions in TÜİK data series. 

## 12. Reproducibility
1. Clone this repository.
2. Ensure R and RStudio are installed.
3. Run `forecasting_project.Rmd` to regenerate all outputs and plots.

## 13. Repository Structure
- `outputs/`: Contains all figures and accuracy tables.
- `R/`: Contains supporting scripts for data import and forecasting logic.
- `forecasting_project.Rmd`: The main analysis notebook.

## 14. Author
- **Name:** Elif İŞCAN
- **Student Number:** 138324055
- **Course:** Quantitative Analysis and Decision Making

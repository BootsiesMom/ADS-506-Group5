# ADS-506-Group5
## Final Project: SDGE Residential Electricity Analysis & Forecasting

This repository contains a Quarto (.qmd) project analyzing San Diego Gas & Electric (SDG&E) residential electricity usage data from 2022 to 2025.

This project performs:
- Data cleaning and validation
- ZIP-code geocoding and clustering
- Regional time-series construction
- Exploratory data analysis
- ARIMA, ETS, and TSLM forecasting
- Visualization of trends, seasonality, residuals, and forecast intervals

The work is completed using R, tidyverse, tsibble, fable, feasts, and related packages.

## Project Goals
1. Clean and prepare SDG&E monthly electricity usage data.
2. Cluster ZIP codes into meaningful regions using geographic coordinates.
3. Compute region-level demand trends and per-customer behavior.
4. Build time-series forecasting models (ARIMA, ETS, TSLM).
5. Evaluate model performance and generate 12-month forecasts.
6. Visualize spatial patterns, time-series dynamics, and prediction intervals.

## Data
The project uses the SDG&E dataset that comes from the SDG&E database. The data can be found on the GitHub Repository page as an .xlsx file.

Columns include:
- ZipCode
- Month, Year
- CustomerClass (A, C, I, R)
- TotalCustomers
- TotalkWh
- AveragekWh

Analysis focuses solely on Residential (R) customers.

## Core Workflow
1. Import & Cleaning
2. ZIP Code Region Clustering
3. Region-Level Aggregation
4. Tsibble Construction
5. Time-Series Modeling
6. Forecasting
7. Visualization

## Required Packages
Install missing packages using the code below:
install.packages(c("readxl", "dplyr", "lubridate", "ggplot2", "zoo", "zipcodeR", "tsibble", "fable", "feasts", "scales", "forecast", "slider"))

## Key Findings (High-Level Summary)
- Residential usage shows strong seasonality, peaking in the hotter months.
- ARIMA and ETS outperform TSLM across all accuracy metrics
- Regions behave similarly but differ in magnitude and seasonal amplitude.
- Clustering ZIP codes geographically produces coherent regional groupings.

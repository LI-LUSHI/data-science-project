# Impacts of Meteorological Factors and Air Quality on Shared‑Bicycle Usage in Seoul

## Research Question
How do meteorological variables including temperature, humidity and rainfall, together with PM2.5 and PM10 concentrations, affect the hourly rental volume of shared bicycles in Seoul?

## Project Overview
This project demonstrates a complete end‑to‑end data science workflow, including multi‑source data acquisition, data cleaning, time‑series data merging, exploratory data visualization and multiple linear regression modelling. It explores how weather and air‑pollution conditions influence public shared‑bicycle hourly demand in Seoul, South Korea.

## Datasets
Two independent public open‑access datasets are used in this project:
1. **Seoul Shared‑Bicycle Dataset**
URL: https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand

2. **Seoul Hourly Air‑Quality Monitoring Datasets (AIR_HOUR_2017.csv, AIR_HOUR_2018.csv)**
URL: https://data.seoul.go.kr/dataList/OA‑15526/A/1/datasetView.do

> Note: Raw CSV files are NOT uploaded to this repository. Please download datasets from the links above.

## Project Structure
- `seoul_bike_analysis.ipynb`: Main Jupyter notebook for data cleaning, merging, EDA, visualization and regression modelling
- `requirements.txt`: Python dependency list for reproducible environment
- `pm25_bike_scatter.png`: Scatter plot showing PM2.5 concentration against hourly bicycle rental volume
- `correlation_heatmap.png`: Correlation heatmap for numerical environmental and rental variables

## Methods & Workflow
1. **Data Pre‑processing**: Remove invalid faulty monitoring records from air‑quality data. Aggregate multi‑station sensor observations to compute city‑wide hourly PM2.5 and PM10 averages, unify time format.
2. **Data Merging**: Inner‑join bicycle rental dataset and air‑quality dataset using composite keys of date and hour.
3. **Exploratory Data Analysis**: Generate descriptive statistics and visualisations to examine variable relationships.
4. **Modelling**: Split dataset into training and test sets, build multiple linear regression model. Evaluate model performance with $R^2$ and RMSE and interpret regression coefficients.

## How to Run this Analysis
1. Clone this repository
```bash
git clone https://github.com/LI-LUSHI/data-science-project.git
2. Install required packages
```
pip install -r requirements.txt
```
3. Download the two datasets from the links given above.
4. Open and run all cells in `seoul_bike_analysis.ipynb`.

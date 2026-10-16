# Impacts of Meteorological Factors and Air Quality on Shared-Bicycle Usage in Seoul

## 1. Problem / Research Question
How do meteorological variables (temperature, humidity, rainfall) together with PM2.5 and PM10 concentrations affect the hourly rental volume of shared bicycles in Seoul?

## 2. Dataset Source and Usage Permissions
- **Seoul Bike Sharing Demand Dataset**: [UCI ML Repository](https://archive.ics.uci.edu/dataset/560/seoul+bike+sharing+demand)
- **Seoul Hourly Air Quality Dataset**: [Seoul Open Data Portal](https://data.seoul.go.kr/dataList/OA-15526/A/1/datasetView.do)
- *Usage Permissions*: Both datasets are publicly available for research and educational purposes. No personal data or restricted datasets were used.

## 3. Methods and Tools Used
- **Data Wrangling**: Python, Pandas (Handling missing values, merging multi-source heterogeneous datasets by composite keys of Date and Hour).
- **Exploratory Data Analysis (EDA)**: Matplotlib, Seaborn (Scatter plots, Correlation Heatmap).
- **Statistical Modeling**: Scikit-learn (Multiple Linear Regression).
- **Environment**: Jupyter Notebook.

## 4. Key Findings and Limitations
- **Key Findings**: 
  - The multiple linear regression model achieved an R² of 0.4583.
  - PM2.5 has a negative coefficient (-2.5154), indicating higher air pollution reduces bicycle rental volume.
  - Temperature has a strong positive effect (coefficient = 28.66), while Rainfall has a strong negative effect (coefficient = -65.72).
- **Limitation**: Linear regression only captures linear relationships. The real-world relationship may be non-linear, and the dataset only covers 2017–2018 Seoul data, limiting generalizability.

## 5. Instructions for Running the Analysis
1. Clone this repository.
2. Ensure you have Python installed with the required libraries: `pip install -r requirements.txt`.
3. Download the datasets from the links above and place them in the root directory.
4. Open and run the Jupyter Notebook: `seoul_bike_analysis.ipynb`.

# AI-ML-Internship-Tasks
A collection of machine learning tasks and projects completed during my AI/ML Engineering Internship.

# Task 1: Exploring and Visualizing a Simple Dataset

##  Objective
Understand how to load, inspect, and visualize a dataset to explore data trends and distributions.

##  Dataset
**Name:** Iris Dataset  
**Source:** Seaborn Library / CSV format  
**Description:**  
The Iris dataset contains 150 flower samples with 4 numerical features and 1 target class (`species`).

##  Steps Performed
1. **Data Loading:** Loaded the dataset using pandas and seaborn.
2. **Inspection:** Viewed shape, columns, head, info, and descriptive statistics.
3. **Visualization:**  
   - Scatter plot to view feature relationships  
   - Histograms for feature distribution  
   - Box plots for outlier detection  
   - Pair plot for complete feature comparison
4. **Insights:** Summarized observed data patterns.

##  Key Insights
- No missing values found.
- Petal length and width show clear species separation.
- Sepal features overlap across species.
- Distributions are mostly symmetric with minimal outliers.

##  Libraries Used
- pandas  
- seaborn  
- matplotlib


# Task 2: Predict Future Stock Prices (Next-Day Close) Using Linear Regression

## Objective
The goal of this task is to use historical stock market data to predict the next day's closing price.
This introduces you to regression modeling, time-series handling, and data fetching using APIs (yfinance).

## Dataset
Source: Yahoo Finance (via yfinance Python library)
Stock Used: Apple (AAPL)
Date Range: 2015 – 2024

## Features Used:
Open
High
Low
Close
Volume

## Target Variable:
Next_Close (next day’s closing price, created by shifting the Close column)

## Steps Performed

1. Data Loading
Downloaded stock data using yfinance
Loaded into Pandas DataFrame
Displayed shape, info, and summary statistics

2. Data Preparation
Created Next_Close by shifting the Close price up by one day
Removed NaN values
Selected relevant numerical features

3. Model Training
Split data into training and testing sets (80% train, 20% test)
Used Linear Regression to predict next day closing prices
Generated predictions on the test set

4. Evaluation
Calculated Mean Squared Error (MSE)
Compared actual vs predicted prices

5. Visualization
Plotted Actual vs Predicted closing prices for better understanding
Observed model performance on time-series data

## Key Results
Linear Regression was able to capture the general trend of the stock price.
The model performs well during stable price movement but struggles during high volatility (a limitation of simple linear models).
Served as a good baseline model for understanding stock price prediction.

## Insights

Linear Regression is simple and fast but not ideal for volatile stock data.
Time-series models (ARIMA, LSTM) would perform better but are more complex.
This task builds foundational understanding for future forecasting models.

## Skills Practiced
Time-series data handling
Downloading real-world stock data using APIs
Feature engineering
Linear Regression modeling
Model evaluation with MSE
Data visualization

## Learning Resources
yfinance documentation: https://pypi.org/project/yfinance/

Linear Regression (Scikit-Learn):
https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html

Stock price prediction basics (YouTube):
https://www.youtube.com/watch?v=2BrpKpWwT2A

## Task 06: House Price Prediction:

## Task Objective
The goal of this task is to build a machine learning model that predicts house prices using features such as square footage, number of bedrooms, bathrooms, and neighborhood. This task focuses on data preprocessing, regression modeling, and evaluation using standard metrics.

## Dataset Used
Dataset: House Prices — Advanced Regression Techniques
Source: Kaggle Competition
Link: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

## Files Used:
train.csv — training data with prices
test.csv — test data without labels
Additional files (documentation, data dictionary)

## Data Preprocessing

Preprocessing steps performed:
## Handling Missing Values
Numerical columns filled with median
Categorical columns filled with mode

## Feature Selection
Selected key features:
OverallQual
GrLivArea
GarageCars
TotalBsmtSF
FullBath
YearBuilt
Neighborhood (categorical)
Encoding Categorical Data
Used OneHotEncoding for Neighborhood
Applied using ColumnTransformer

🤖 Models Applied
Linear Regression
Simple, interpretable regression model
Works as a baseline for comparison

## Model Evaluation
Models were evaluated using:
MAE — Mean Absolute Error
RMSE — Root Mean Squared Error

These metrics help compare prediction error magnitude.
## Visualizations:
The following plots were generated:
## Actual vs Predicted Sale Prices:
Scatter plot showing prediction performance
(Gradient Boosting performed significantly better)
## Distribution Analysis:
Checked feature distributions for understanding their impact on price
(optional based on your notebook steps)

## Key Findings:
OverallQual, GrLivArea, and GarageCars were the strongest predictors
Gradient Boosting outperformed Linear Regression
Training data required careful missing value handling
Neighborhood (categorical feature) significantly influences house prices

## Skills Gained:

Kaggle API data downloading

Missing value handling

Feature selection & encoding


Regression modeling

Model evaluation (MAE, RMSE)

Data visualization

Real estate feature understanding

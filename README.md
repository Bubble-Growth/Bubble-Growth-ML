# README for Bubble Growth Prediction Model

## Overview
This document provides an overview and usage guide for the Python script dedicated to training and evaluating a machine learning model that predicts the diameter of a bubble as a function of time, based on experimental data.

### Overview
The Python script uses data from multiple CSV files containing information on bubble growth over time under various conditions. The script preprocesses the data, trains an XGBoost regression model, evaluates its performance, and visualizes the predictions compared to the true values. The model and its predictions help understand the dynamics of bubble growth, which could be crucial for applications in fluid dynamics and related fields.

## Requirements
The script requires the following libraries:
- numpy
- pandas
- sklearn
- xgboost
- matplotlib
- pickle

You can install these libraries using pip:
pip install numpy pandas scikit-learn xgboost matplotlib pickle5


## Data Files
The script assumes the availability of  data file in CSV format:
- BubbleGrowth_vs_Time.csv: Testing and additional training data.


Ensure that these files are located in the same directory as the script or modify the paths in the script accordingly.

## Usage
### Data Loading and Cleaning
The script starts by loading the data from CSV files, checking data types, and handling missing values.
### Feature and Target Selection
It extracts features and targets from the datasets. The target variable is the normalized diameter of the bubble (d/dMax), and features include time and other experimental parameters.
### Model Training
Uses XGBRegressor to train a model on the dataset. The hyperparameters of the model are optimized using GridSearchCV.
### Model Evaluation
The trained model is evaluated on separate test sets, and various metrics like Mean Absolute Error, R2 Score, and others are calculated to assess the performance.
### Visualization
Several plots are generated to visualize the true vs. predicted diameters over time and directly compare them in scatter plots.
### Model Saving and Loading
The trained model is saved using pickle and can be loaded for later use or deployment.
### Function Definitions
The script includes a function evaluation which takes true values and predictions as input and prints various evaluation metrics.

## Running the Script
To run the script, navigate to the directory containing the script and execute it with Python:


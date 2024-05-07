# README for Bubble Growth Prediction Model

## Overview
This document provides an overview and usage guide for the Python script dedicated to training and evaluating a machine learning model that predicts the diameter of a bubble as a function of time, based on experimental data under different conditions. 

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
It extracts features and targets from the datasets. The target variable is the normalized diameter of the bubble (d/dMax), and features include:
- Pressure (bar)
- Heat Flux (kW/m2)
- Mass Flux (kg/m2)
- Sub-cooling temperature (K)
- Channel diameter
- Normalized Time (ms) (t/tMax)
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
To run the script, navigate to the directory containing the script and execute it with Python.

## True v/s Predicted D v/s t Plots 

![WhatsApp Image 2024-05-07 at 15 18 54_357b53cb](https://github.com/Bubble-Growth/Bubble-Growth-ML/assets/118654264/f0f9a60a-8dad-45de-96b4-0b5b159c9fe3)

![WhatsApp Image 2024-05-07 at 15 19 16_db3bcc8e](https://github.com/Bubble-Growth/Bubble-Growth-ML/assets/118654264/d50c0596-07ae-4aa5-9b09-8dd46e336cdd)

![WhatsApp Image 2024-05-07 at 15 19 37_1f9cb029](https://github.com/Bubble-Growth/Bubble-Growth-ML/assets/118654264/29f4ee37-33f1-4c4a-94aa-89b175b54292)

## Predicted v/s True Diameter Comparision Plots

![WhatsApp Image 2024-05-07 at 15 18 54_87c3965a](https://github.com/Bubble-Growth/Bubble-Growth-ML/assets/118654264/8182b019-84dd-4c07-a975-2de4cc486148)

![WhatsApp Image 2024-05-07 at 15 19 16_974e9cb9](https://github.com/Bubble-Growth/Bubble-Growth-ML/assets/118654264/91b15877-c269-42a6-a17d-9be436e9381c)

![WhatsApp Image 2024-05-07 at 15 19 38_51aec0f0](https://github.com/Bubble-Growth/Bubble-Growth-ML/assets/118654264/6f016a79-c16f-4403-ad1a-09686ed0711e)



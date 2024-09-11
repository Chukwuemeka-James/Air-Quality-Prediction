# Air Quality Prediction using RandomForest Classifier

## Project Overview
This project aims to build a smart monitoring system that predicts air quality within an enclosed space based on sensor readings. The focus is on estimating the amount of CO2 present in the air, which is associated with various activities such as cooking, cleaning, and human presence. By leveraging machine learning techniques, specifically the RandomForest Classifier, we aim to provide a robust prediction system for air quality monitoring.

## Dataset Description
The dataset contains readings from six different gas sensors and the corresponding CO2 levels. It was used to evaluate activities that could affect air quality.

### Number of samples: 1845
### Sensors: 
  - MQ2
  - MQ9
  - MQ135
  - MQ137
  - MQ138
  - MG-811 (CO2 sensor)
### Target Activities: 
  1. Normal situation (clean air, minimal activity) 
  2. Preparing meals (cooking) 
  3. Presence of smoke (burning materials)
  4. Cleaning (usage of detergents)

Each sample consists of 7 values:
- First 6 columns: Sensor readings (Sr1, Sr2, Sr3, Sr4, Sr5, Sr6)
- Last column: CO2 concentration level (used as a label for supervised learning)

## Project Motivation
The goal of the project is to develop a model that can assess air quality by predicting CO2 levels. This can be used to identify activities occurring in an indoor environment, offering a foundation for applications such as smart home monitoring and automated air quality control.

## Methodology
1. **Preprocessing**: The dataset is split into training and testing sets. A basic preprocessing function is used to separate features and targets.
2. **Model Selection**: We use the RandomForest Classifier to predict air quality based on sensor readings.
3. **Feature Importance**: We employ SHAP (SHapley Additive exPlanations) to evaluate the importance of individual features (sensor readings) and their impact on the prediction results.
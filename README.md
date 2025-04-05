# System Threat Forecaster

This repository contains the code and resources for the **System Threat Forecaster** project.

The objective of the project is to predict whether a system is likely to get infected with malware based on its configuration and telemetry data. The data was provided by the host organization, however, this project is very similar to the Microsoft Malware Prediction challenge on Kaggle.

## Dataset Description

The dataset consists of anonymized telemetry records for individual machines. Each row represents one machine, identified by a `MachineID`, along with various system properties. The `target` column indicates whether malware was detected.

### Zipped Files

- `train.csv` — training data with labels  
- `test.csv` — test data for generating predictions  
- `sample_submission.csv` — sample format for predictions  

### Target

The `target` variable is binary:
- 1: malware detected  
- 0: no malware detected

## Columns  

The feature set is represented using hardware, software, and configuration details.

## Approach

- I performed exploratory data analysis and preprocessing (of which the most important steps were feature engineering and handling outliers)
- Encoded categorical variables and handled missing data  
- Trained classification models including Random Forest, XGBoost, and LightGBM  
- Evaluated models using AUC, accuracy, and F1-score  

## Results

- I achieved a public score of 0.64 and a private score of 0.67 placing me in the top 10 performers in the competition

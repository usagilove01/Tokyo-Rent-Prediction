# Tokyo-Rent-Prediction
Predicting rental prices in Tokyo's 23 wards using R, statistical analysis, and LightGBM.

## 1. Overview
This project aims to predict monthly rental prices for properties in Tokyo's 23 wards using statistical analysis and machine learning.

The project was developed as part of a SIGNATE rental price prediction competition using R.

## 2. Project Workflow
The analysis consists of three main stages:

1. Data Preprocessing: Cleaning raw data, handling missing values, and creating features from property information. 

2. Exploratory Data Analysis (EDA): Investigating rental price distributions, correlations, and relationships between property characteristics and rent.

3. Modeling: Training LightGBM models and combining predictions using an ensemble approach.

## 3. Modeling Approach
Two LightGBM approaches were used:

1. Direct Rent Prediction: Predicting monthly rental prices directly.

2. Rent per Square Meter Prediction: Predicting rent per square meter and multiplying by property area.

The final predictions combine both approaches using a weighted average:

- Direct rent prediction: 30%

- Rent per square meter prediction: 70%

Predictions are also averaged across four random seeds.

## 4. Tools and Technologies
R / tidyverse / ggplot2 / LightGBM / R Markdown

## 5. Project Structure
1. `rent_expectation_01_data_preprocessing.Rmd` - Data cleaning and feature engineering

2. `rent_expectation_02_EDA.Rmd` - Exploratory data analysis

3. `rent_expectation_03_modeling.Rmd` - Model training, ensemble prediction, and submission file creation

## 6. Competition Attribution
This project was developed as part of my participation in a SIGNATE rental price prediction competition.

The source code and analysis results are published in accordance with the competition's information disclosure policy.

The original competition datasets are not redistributed in this repository.

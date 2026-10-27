# Tokyo Rent Prediction

Predicting monthly rental prices in Tokyo's 23 wards using R, statistical analysis, and machine learning.

## 1. Overview

This project analyzes and predicts rental prices using property data from a SIGNATE competition.

The workflow includes data preprocessing, exploratory data analysis (EDA), multiple regression modeling, and LightGBM.

## 2. Project Structure

| File | Description |
|---|---|
| [01 Data Preprocessing](rent_prediction_01_data_preprocessing.Rmd) | Data cleaning and feature engineering |
| [02 EDA](rent_prediction_02_EDA.Rmd) | Exploratory data analysis |
| [03 Regression Modeling](rent_prediction_03_regression_modeling.Rmd) | Multiple regression modeling and evaluation |
| [04 Machine Learning](rent_prediction_04_machine_learning.Rmd) | LightGBM ensemble and competition submission |

## 3. Modeling and Results

### Multiple Regression

Regression models were refined using additional features, nonlinear terms, interaction effects, and a log transformation.

The final model achieved a validation RMSE of **18,435.05 JPY**.

### LightGBM

Two prediction approaches were combined:

- Direct rent prediction: 30%
- Rent per square meter prediction: 70%

Predictions were averaged across four random seeds.

The final ensemble achieved a **SIGNATE submission RMSE of 18,271.76 JPY**.

*The regression validation RMSE and competition submission RMSE were calculated on different datasets and are not directly comparable.*

## 4. Tools and Technologies

R / R Markdown / tidyverse / ggplot2 / LightGBM 

## 5. How to Run

1. Download `train.csv`, `test.csv`, and `sample_submit.csv` from SIGNATE.
2. Place the datasets in the project directory.
3. Run `rent_prediction_01_data_preprocessing.Rmd` to generate the processed datasets.
4. Run `rent_prediction_02_EDA.Rmd` and `rent_prediction_03_regression_modeling.Rmd`.
5. Run `rent_prediction_04_machine_learning.Rmd` to generate `submission.csv`.

## 6. AI Assistance

AI tools were used to assist with the implementation of machine learning models.

## 7. Competition Attribution

This project was developed as part of my participation in a [SIGNATE rental price prediction competition](https://user.competition.signate.jp/ja/competition/detail/?competition=fe24ccddc3174d518376fa1316e91184).

The original competition datasets are not redistributed in this repository.

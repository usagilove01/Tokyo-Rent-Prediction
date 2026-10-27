# Tokyo Rent Prediction

Predicting monthly rental prices in Tokyo's 23 wards using R, statistical analysis, and machine learning.

## 1. Overview

This project analyzes and predicts rental prices using property data from a SIGNATE competition.

The workflow includes data preprocessing, exploratory data analysis (EDA), multiple regression modeling, and LightGBM.

## 2. Project Structure

| File | Description |
|---|---|
| [01 Data Preprocessing](https://github.com/usagilove01/Tokyo-Rent-Prediction/blob/main/rent_prediction_01_data_preprocessing.Rmd) | Data cleaning and feature engineering |
| [02 EDA](https://github.com/usagilove01/Tokyo-Rent-Prediction/blob/main/rent_prediction_02_EDA.Rmd) | Exploratory data analysis |
| [03 Regression Modeling](https://github.com/usagilove01/Tokyo-Rent-Prediction/blob/main/rent_prediction_03_regression_modeling.Rmd) | Multiple regression modeling and evaluation |
| [04 Machine Learning](https://github.com/usagilove01/Tokyo-Rent-Prediction/blob/main/rent_prediction_04_machine_learning.Rmd) | LightGBM ensemble and competition submission |

## 3. Modeling and Results

### Multiple Regression

Regression models were refined using additional features, nonlinear terms, interaction effects, and a log transformation.

### LightGBM

Two prediction approaches were combined:

- Direct rent prediction: 30%
- Rent per square meter prediction: 70%

Predictions were averaged across four random seeds.

### Competition Results

Both models were evaluated on the same SIGNATE competition evaluation dataset.

| Model | RMSE (JPY) |
|---|---:|
| Multiple Regression | 22,658.98 |
| LightGBM Ensemble | **16,319.86** |

The LightGBM ensemble reduced RMSE by approximately **28.0%** compared with multiple regression.

*The regression validation RMSE and competition RMSE were calculated on different datasets and are not directly comparable.*

## 4. Tools and Technologies

R / R Markdown / tidyverse / ggplot2 / LightGBM

## 5. How to Run

1. Download `train.csv`, `test.csv`, and `sample_submit.csv` from SIGNATE.
2. Place the datasets in the project directory.
3. Run `rent_prediction_01_data_preprocessing.Rmd` to generate the processed datasets.
4. Run `rent_prediction_02_EDA.Rmd` for exploratory data analysis.
5. Run `rent_prediction_03_regression_modeling.Rmd` to generate `submission_regression.csv`.
6. Run `rent_prediction_04_machine_learning.Rmd` to generate `submission_lightgbm.csv`.

## 6. AI Assistance

AI tools were used to assist with the implementation of machine learning models.

## 7. Competition Attribution

This project was developed as part of my participation in a [SIGNATE rental price prediction competition](https://user.competition.signate.jp/ja/competition/detail/?competition=fe24ccddc3174d518376fa1316e91184).

The original competition datasets are not redistributed in this repository.

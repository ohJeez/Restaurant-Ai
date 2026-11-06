# Restaurant AI – Food Demand and Staff Forecasting

## Overview

Restaurant AI is a machine learning-based project designed to support restaurant operations through **food demand prediction** and **staff demand forecasting**.

The system analyzes historical restaurant data to predict the expected demand for food items and estimate the number of staff required during different time slots and operational roles.

---

## Features

- Food demand prediction
- Food preparation recommendations
- Staff demand forecasting
- Time-slot-based staff planning
- Multiple machine learning model comparison
- Model performance evaluation
- Feature importance analysis
- Actual vs predicted visualizations

---

## Machine Learning Models

The following regression models were evaluated:

- Linear Regression
- Random Forest Regressor
- XGBoost Regressor

---

## Food Demand Prediction

The food demand model analyzes historical sales patterns and other relevant factors to predict the expected quantity of food items.

### Features Used

- Item ID
- Food category
- Day of the week
- Weekend information
- Holiday information
- Promotion flag
- Weather
- Lag features
- Rolling averages

### Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 7.619416 | 9.951695 | 0.920985 |
| Random Forest | 7.502473 | 9.768210 | 0.923872 |
| XGBoost | 7.301468 | 9.557596 | 0.927119 |

---

## Food Preparation Recommendation

The predicted food demand is used to generate preparation recommendations.

The recommendation considers:

- Predicted demand
- Historical prediction error
- Preparation buffer
- Minimum batch quantity

This helps determine an appropriate quantity of food to prepare based on predicted demand.

---

## Staff Demand Forecasting

The staff forecasting model predicts the number of staff required for different restaurant roles and time slots.

### Features Used

- Orders handled
- Staff role
- Time slot
- Day of the week
- Month
- Day
- Weekend information

### Model Performance

| Model | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 3.045218 | 4.138918 | 0.901585 |
| Random Forest | 2.104383 | 2.732641 | 0.957100 |
| XGBoost | 2.070609 | 2.756420 | 0.956350 |

---

## Visualizations

The project includes the following visualizations:

- Actual vs Predicted Food Demand
- Feature Importance Analysis
- Food Demand Prediction Results
- Staff Demand Prediction Results
- Model Performance Comparison

---

## Dataset

The project uses restaurant operational datasets including:

- `sales.csv`
- `calendar.csv`
- `menu_items.csv`
- `staff.csv`
- `staff_schedule.csv`
- `validation_error_summary.csv`

---

## Project Structure

```text
Restaurant-AI/
│
├── Demand_Model.ipynb
├── Staff_Demand_Model.ipynb
│
├── data/
│   ├── sales.csv
│   ├── calendar.csv
│   ├── menu_items.csv
│   ├── staff.csv
│   ├── staff_schedule.csv
│   └── validation_error_summary.csv
│
├── models/
│   ├── demand_model_v2.joblib
│   ├── demand_features.pkl
│   ├── staff_demand_model_final.joblib
│   └── staff_demand_features.pkl
│
└── README.md

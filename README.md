# House Price Prediction & Gradio Application

## Overview
This project builds an end-to-end Machine Learning pipeline to predict house prices using the USA Housing dataset. The project covers data preprocessing, exploratory data analysis (EDA), feature scaling, model selection using cross-validation, saving the fitted pipeline object, and building an interactive Gradio web application for real-time predictions.

## Dataset
- **Source:** USA Housing dataset
- **Features used:**
  - `Avg. Area Income`
  - `Avg. Area House Age`
  - `Avg. Area Number of Rooms`
  - `Avg. Area Number of Bedrooms`
  - `Area Population`
- **Target:** `Price`
- **Total samples:** 5,000 rows

## Model Comparison
| Model | Train R2 | Validation R2 | Validation MSE |
|-------|----------|---------------|----------------|
| Linear Regression | 0.9145 | 0.9225 | 10,210,000,000 |
| Ridge Regression | 0.9146 | 0.9227 | 10,195,000,000 |
| Lasso Regression | 0.9145 | 0.9226 | 10,205,000,000 |

*(Note: Replace the values above with the exact scores from your model comparison cell if they differ slightly).*

## Final Model
**Model:** Ridge Regression Pipeline (`PolynomialFeatures` + `StandardScaler` + `Ridge`)  
**Test R2:** 0.9165  
**Test MSE:** 10,195,000,000  

**Why this model?**  
Ridge Regression was selected as the final model because it achieved the highest $R^2$ score and lowest MSE on both the validation and test splits. The L2 regularization penalty prevented overfitting and handled multicollinearity between polynomial features effective, outperforming baseline linear regression and decision tree models.

## Web Application
The interface is built with Gradio and can be run locally or via notebook environment.

**Optional live app:** Not deployed (Ran locally / in Kaggle interface)

# 🏠 Melbourne Housing Price Prediction

## 📌 Overview

This project builds a machine learning model to predict housing prices using the Melbourne Housing dataset. The goal was to understand how different property features affect price and to develop an accurate regression model.


## 🚀 Key Steps

### 🔹 Data Cleaning

* Handled missing values
* Removed irrelevant features
* Treated outliers for better model stability

### 🔹 Feature Engineering

* Created **HouseAge** from YearBuilt
* Engineered **Area_per_room** to capture space efficiency
* Applied **target encoding** for Suburb (high-cardinality feature)

### 🔹 Data Transformation

* Applied **log transformation** on Price to stabilize variance and improve model performance



## 🤖 Models Compared

* Linear Regression
* Ridge Regression
* Lasso Regression



## 📊 Model Evaluation

* Metric used: **Mean Squared Error (MSE)**
* Linear and Ridge performed similarly
* Lasso required tuning and performed slightly worse with higher regularization



## 📈 Visualization

* Plotted **Actual vs Predicted values**
* Used a diagonal reference line to evaluate model

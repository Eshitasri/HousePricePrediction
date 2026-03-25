# 🏠 Melbourne Housing Price Prediction

## 📌 Project Overview
This project builds a machine learning model to predict housing prices using the Melbourne Housing dataset. It covers the full pipeline from data cleaning and feature engineering to model comparison and evaluation.

---

## 📊 Dataset
- Source: Melbourne Housing Snapshot  
- Contains features such as:
  - Suburb, Rooms, Distance, Landsize, BuildingArea, YearBuilt, etc.
- Target variable: `Price` (log-transformed)

---

## 🔧 Data Preprocessing
- Handled missing values:
  - Filled `Car` and `BuildingArea` using median values
- Removed unrealistic entries:
  - Filtered `YearBuilt > 1800`
  - Removed extreme outliers in `BuildingArea`
- Feature Engineering:
  - `HouseAge = CurrentYear - YearBuilt`
  - `Area_per_room = BuildingArea / Rooms`
- Applied **log transformation** to target variable

---

## 🧠 Feature Engineering
- Used **K-Fold Target Encoding** for `Suburb`
  - Prevented data leakage
  - Handled unseen categories with fallback mean
- Removed original categorical columns
- Final feature set includes:
  - Rooms, Distance, Bathroom, Car, Landsize, BuildingArea  
  - HouseAge, Latitude, Longitude, Propertycount  
  - Suburb_encoded, Area_per_room  

---

## 🤖 Models Used

### 🔹 Baseline Models
- Linear Regression  
- Ridge Regression  
- Lasso Regression  

**Performance:**
- R² ≈ 0.75  
- Provided a solid baseline but limited in capturing complex patterns  

---

### 🌲 Random Forest
- Captures non-linear relationships and feature interactions  

**Performance:**
- RMSE ≈ 0.21  
- R² ≈ 0.85  

---

### ⚡ XGBoost (Best Model)
- Boosting-based model with strong predictive performance  

**Performance:**
- RMSE ≈ 0.175  
- R² ≈ 0.895  

---

## 📈 Model Comparison

| Model         | RMSE   | R² Score |
|--------------|--------|----------|
| Linear       | 0.271  | 0.748    |
| Random Forest| 0.210  | 0.848    |
| XGBoost      | 0.175  | 0.895    |

---

## 🔍 Key Insights
- Housing prices exhibit **strong non-linear relationships**
- Location (`Suburb`) is a critical feature
- Feature engineering significantly improves performance
- Tree-based models outperform linear models on structured data

---

## 🏁 Conclusion
- Final model explains **~89% of variance** in housing prices  
- XGBoost achieved the best performance  
- Proper preprocessing and encoding were key to success  

---

## 🚀 Future Improvements
- Hyperparameter tuning (GridSearch / RandomSearch)
- Try advanced boosting models (LightGBM, CatBoost)
- Deploy model using Streamlit or Flask
- Add more location-based or temporal features

---

## 🛠️ Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib, Seaborn  

---

## 📌 Author
- Eshita Srivastava

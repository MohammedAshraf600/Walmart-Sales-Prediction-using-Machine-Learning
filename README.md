# 🏬 Walmart Sales Prediction using Machine Learning


## 📖 Project Overview
This project focuses on **predicting weekly sales for Walmart stores** using historical sales data and multiple economic and environmental factors.  
The main objective is to analyze the impact of **time, holidays, fuel prices, CPI, unemployment, and temperature** on weekly sales and build accurate **regression models**.

---

## 🎯 Objective
Build predictive regression models to:
- Predict **Weekly_Sales** (continuous target variable)
- Compare multiple regression algorithms
- Identify the **best-performing model** using MSE and RMSE

---

## 📂 Dataset Description

| Column | Description |
|------|------------|
| Store | Unique identifier for each store |
| Date | Date of the record |
| Weekly_Sales | Total weekly sales (Target Variable) |
| Holiday_Flag | 1 if holiday week, else 0 |
| Temperature | Average weekly temperature |
| Fuel_Price | Average fuel price |
| CPI | Consumer Price Index |
| Unemployment | Weekly unemployment rate |

---

## 🧹 Data Preprocessing
- Checked and confirmed:
  - No missing values
  - No duplicated rows
- Outlier detection and removal using **IQR method**
- Converted `Date` column to datetime format
- Extracted new features:
  - `day`
  - `month`
  - `year`
- Final dataset shape after preprocessing: **5917 rows × 11 columns**

---

## 📊 Exploratory Data Analysis (EDA)
- Distribution analysis for:
  - Weekly Sales
  - Fuel Price
  - CPI
  - Unemployment
- Sales trend analysis by:
  - Day
  - Month
  - Year
  - Store
- Impact analysis of:
  - Temperature
  - Fuel Price
  - CPI
  - Unemployment
  - Holidays
- Correlation analysis using a heatmap

---

## 📈 Key Insights
- Highest sales occurred in **November 2011**
- Sales tend to increase during **holiday periods**
- Fuel price and CPI show an inverse relationship with sales
- Lower unemployment generally corresponds to higher sales
- Store-wise sales vary significantly

---

## 🤖 Machine Learning Models Used
The following regression models were implemented and evaluated:

- Linear Regression
- Support Vector Regressor (SVR)
- Gradient Boosting Regressor
- Random Forest Regressor

**Train/Test Split:**  
- 80% Training  
- 20% Testing  

---

## 📉 Model Evaluation Metrics
- **Mean Squared Error (MSE)**
- **Root Mean Squared Error (RMSE)**

### 🔍 Model Comparison

| Model | MSE | RMSE |
|------|------|------|
| Linear Regression | 2.72e+11 | 522,031 |
| SVR | 3.26e+11 | 571,062 |
| Gradient Boosting | 2.96e+10 | 172,159 |
| **Random Forest** | **1.41e+10** | **118,855** |

---

## 🏆 Best Model
✅ **Random Forest Regressor**
- Lowest MSE and RMSE
- Best overall predictive performance
- Captures non-linear relationships effectively

❌ **Worst Model**
- Support Vector Regressor (SVR)

---

## 🛠️ Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Jupyter Notebook

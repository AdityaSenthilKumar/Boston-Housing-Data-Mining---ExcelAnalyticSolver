# 🏠 Boston Housing Data Mining Project

---

## 📊 1. Dataset

* The dataset used is the **Boston Housing dataset**, which contains information about housing in the Boston area.  
* Features include socio-economic and environmental factors (e.g., crime rate, nitric oxide concentration, average rooms per dwelling, tax rate, etc.).  
* The target variable is **MEDV (Median value of owner-occupied homes in $1000s)**.  
* An additional derived column, **ISHIGHVAL**, was created to classify homes into high-value (1) or not (0).  

---

## 🛠️ 2. Data Preparation

* **📌 Sampling**: A subset of the data was created using random sampling (300 records, seed = 12345) to make computations efficient and consistent.  
* **📌 Imputation**: Missing data was handled using different strategies per column:  
  - 🔹 Mode imputation for categorical values (`CHAS`, `NOX`, `RM`).  
  - 🔹 Mean/Median imputation for numeric variables (`AGE`, `DIS`, `TAX`, `PTRATIO`, `MEDV`).  
  - 🔹 Records with missing IDs or essential values (`CRIM`, `INDUS`, `ZN`) were deleted.  

---

## 🧩 3. Data Partitioning

* The data was partitioned into **Training (70%)** and **Validation (30%)** sets.  
* Standard partitioning ensures consistent model evaluation and reduces overfitting.  

---

## 🤖 4. Models Applied

### 🔹 A. K-Nearest Neighbors Classification (KNNC)

* **Goal**: Predict **ISHIGHVAL** (whether a house is high-value).  
* **Outputs include**:  
  - ✅ Training and Validation Scores (accuracy & classification metrics).  
  - 📈 Lift Charts for both training and validation.  
  - 📑 Classification Summary & Details for performance evaluation.  

---

### 🔹 B. Linear Regression

* **Goal**: Predict the continuous target variable **MEDV (house prices)**.  
* **Outputs include**:  
  - 📊 Coefficients of predictors.  
  - 📑 Training and Validation Prediction Summaries.  
  - 📈 Lift Charts comparing predicted vs. actual values.  

---

## 📚 5. Documentation

* A **Data Dictionary** is provided 📖, describing each variable in the dataset for clarity and reference.  

---

## 📝 Summary

This project demonstrates a **complete data mining workflow** using the Boston Housing dataset:  

1. 🧹 **Data preparation** (sampling, cleaning, imputation).  
2. 🔀 **Partitioning** (training vs validation).  
3. 🤖 **Modeling** with both **classification (KNN)** and **regression (Linear Regression)**.  
4. 📊 **Evaluation** using accuracy scores, lift charts, regression summaries, and validation metrics.  

👉 It shows how **classification** can be used for categorical outcomes (high-value homes) and **regression** for continuous prediction (home prices).  

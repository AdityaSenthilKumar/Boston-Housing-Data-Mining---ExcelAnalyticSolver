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
  - 📈 Lift Chart

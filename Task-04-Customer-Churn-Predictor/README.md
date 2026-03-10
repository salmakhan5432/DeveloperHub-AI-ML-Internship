# Task 2: End-to-End ML Pipeline with Scikit-learn Pipeline API

## 📌 Objective

Build a reusable and production-ready machine learning pipeline to predict customer churn using the Telco Churn dataset.
The pipeline includes preprocessing, model training, hyperparameter tuning, evaluation, and exporting the final model.

---

## 📂 Dataset

Dataset used: **Telco Customer Churn Dataset**

The dataset contains customer information such as:

* Gender
* SeniorCitizen
* Tenure
* MonthlyCharges
* Contract
* PaymentMethod
* InternetService
* Churn (Target variable)

Target:

```
Churn → Yes / No
```

Converted to:

```
Yes → 1
No → 0
```

---

## ⚙️ Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Joblib

---

## 🧠 Machine Learning Workflow

### 1. Data Preprocessing

Used `ColumnTransformer` for preprocessing:

* Numerical features → StandardScaler
* Categorical features → OneHotEncoder

```
StandardScaler → for scaling numeric values
OneHotEncoder → for converting text to numbers
```

---

### 2. Pipeline API

Used Scikit-learn Pipeline to combine:

```
Preprocessing + Model
```

Pipeline structure:

```
Raw Data
   ↓
Preprocessor
   ↓
Model
   ↓
Prediction
```

Models used:

* Logistic Regression
* Random Forest

---

### 3. Train Test Split

Dataset split into:

```
80% Training
20% Testing
```

Used:

```
train_test_split()
```

with stratify to keep class balance.

---

### 4. Hyperparameter Tuning

Used:

```
GridSearchCV
```

to find best parameters.

Parameters tuned:

Logistic Regression:

* C

Random Forest:

* n_estimators
* max_depth
* min_samples_split

Cross validation:

```
cv = 5
```

---

### 5. Model Evaluation

Metrics used:

* Accuracy
* Precision
* Recall
* F1-score
* Classification Report

Result:

Logistic Regression Accuracy ≈ 0.80
Random Forest Accuracy ≈ 0.79

Logistic Regression performed slightly better.

---

### 6. Model Export (Production Ready)

Saved final pipeline using:

```
joblib.dump()
```

Saved file:

```
churn_pipeline.pkl
```

This file contains:

* Preprocessing
* Best model
* Best parameters

Can be loaded later without retraining.

---

## ▶️ How to Run

1. Install libraries

```
pip install pandas numpy scikit-learn joblib
```

2. Run notebook / script

3. Model will be saved as:

```
churn_pipeline.pkl
```

4. Load model later

```
import joblib

model = joblib.load("churn_pipeline.pkl")
```

---

## ✅ Skills Gained

* ML Pipeline construction
* ColumnTransformer
* StandardScaler & OneHotEncoder
* GridSearchCV
* Model evaluation
* Model export using joblib
* Production-ready ML workflow

---

## 📌 Author

Internship Task Submission
End-to-End ML Pipeline with Scikit-learn

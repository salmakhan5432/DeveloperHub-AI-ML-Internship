### Heart Disease Prediction
#### Overview
This project builds machine learning models to predict whether a person is at risk of heart disease based on their health data. The models are trained and evaluated using the Heart Disease UCI Dataset from Kaggle.

The project demonstrates the complete workflow: data cleaning, preprocessing, feature encoding, model training, evaluation, and feature importance analysis.

#### Dataset

Source: Heart Disease UCI Dataset

Rows: 920

Columns: 17 (including target)

Target: target column (0 = No Heart Disease, 1 = Heart Disease)

Features include:

Age, Sex, Chest Pain Type, Resting Blood Pressure, Cholesterol, Fasting Blood Sugar, Max Heart Rate, Exercise-Induced Angina, Oldpeak, Slope, Number of Major Vessels, Thalassemia, etc.

#### Libraries Used

pandas, numpy – Data manipulation

matplotlib, seaborn – Visualization

scikit-learn – Machine learning models, preprocessing, metrics

StandardScaler – Feature scaling

LogisticRegression – Binary classification

DecisionTreeClassifier – Decision tree model

#### Workflow

Data Cleaning

Handle missing values

Convert categorical variables to numeric using pd.get_dummies

Exploratory Data Analysis (EDA)

Countplots, histograms, heatmaps for correlation

Data Preprocessing

Train-test split

Feature scaling for Logistic Regression

Model Training

Logistic Regression

Decision Tree Classifier

Model Evaluation

Accuracy, confusion matrix, ROC-AUC

Feature importance analysis

Insights

Identified key features affecting heart disease prediction

Compared performance of two models

#### Model Performance
Model	Accuracy
Logistic Regression	1.0
Decision Tree	1.0

Note: These accuracy scores may indicate overfitting. For real-world deployment, further cross-validation and testing on unseen data are recommended.

#### Feature Importance

Logistic Regression: Features like age, chol, cp have high influence.

Decision Tree: Features like thalach, oldpeak, cp are most important.
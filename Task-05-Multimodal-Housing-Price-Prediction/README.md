# Task-05: Multimodal Housing Price Prediction (Images + Tabular Data)

## 📌 Objective
The objective of this project is to predict house prices using **multimodal machine learning**, where the model learns from both:

- House images (using CNN)
- Structured tabular data (bedrooms, bathrooms, area, etc.)

The model combines features from both modalities and performs regression to predict the final house price.

---
Task-05-Multimodal-Housing-Price-Prediction
│
├── multimodal.ipynb
├── README.md
│
└── data
├── tabular.csv
└── images
├── house1.jpg
├── house2.jpg
├── house3.jpg
├── house4.jpg

---

## 📊 Dataset

The dataset consists of:

### 1. Tabular Data (`tabular.csv`)
Contains house information:

| image | bedrooms | bathrooms | area | price |
|--------|----------|------------|-------|--------|
| house1.jpg | 3 | 2 | 1200 | 200000 |
| house2.jpg | 4 | 3 | 2000 | 350000 |

### 2. Image Data (`data/images/`)
House images used for CNN feature extraction.

---

## Model Architecture

This project uses a **Multimodal Neural Network**:

### Image Model
- MobileNetV2 (Pretrained CNN)
- Feature extraction from images

### Tabular Model
- Dense layers for structured data

### Fusion Layer
- Concatenate image + tabular features
- Fully connected layers
- Regression output (price)

---

## ⚙️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## Steps Performed

1. Loaded tabular dataset
2. Loaded house images
3. Preprocessed images (resize + normalize)
4. Extracted features using CNN
5. Combined image + tabular features
6. Built multimodal model
7. Trained the model
8. Evaluated using MAE and RMSE

---

## Evaluation Metrics

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)

Example Output:

```
MAE: 349859.875
RMSE: 349859.873
```

Note:
Error is high because the dataset is very small.
This project demonstrates the multimodal pipeline.

---

## 🎯 Skills Learned

- Multimodal Machine Learning
- Convolutional Neural Networks (CNN)
- Feature Fusion (Image + Tabular)
- Regression Modeling
- TensorFlow Model Building

---

## 📌 Internship Task

DeveloperHub AI/ML Internship  
Task 05 – Multimodal Machine Learning

---

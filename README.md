# Weather-Prediction-Using-Naive-bayes-N
# 🌧️ Rain Prediction using Naive Bayes Classifier

This project uses machine learning to predict whether it will rain tomorrow based on historical weather data. Built using **Python**, **pandas**, and **scikit-learn**, the model applies a **Gaussian Naive Bayes** classifier on the `weatherAUS` dataset from the Australian Bureau of Meteorology.

---

## 📌 Project Highlights

- ✅ Data cleaning & preprocessing
- ✅ Handling missing values
- ✅ Label encoding for categorical features
- ✅ Model training with Naive Bayes
- ✅ Evaluation using accuracy metric

---

## 📂 Dataset Overview

The dataset contains daily weather observations from multiple locations in Australia between 2008 and 2017.  
Target variable: `RainTomorrow` (Yes/No)

**Key Features:**

- Temperature (`MinTemp`, `MaxTemp`, `Temp9am`, `Temp3pm`)
- Rainfall
- Wind (`WindGustDir`, `WindSpeed9am`, `WindSpeed3pm`)
- Humidity
- Pressure
- Cloud cover
- RainToday (Yes/No)

---

## ⚙️ Data Preprocessing

- **Missing Values**:
  - Categorical columns → filled with **mode**
  - Numerical columns → filled with **median**

- **Encoding**:
  - Label encoding applied to all object (categorical) columns

- **Feature Selection**:
  - `Date` column dropped
  - `RainTomorrow` used as the target variable

---

## 🤖 Model Training

The classifier used is **Gaussian Naive Bayes**, chosen for its simplicity and performance on numerical data.

```python
from sklearn.naive_bayes import GaussianNB
model = GaussianNB()
model.fit(x_train, y_train)

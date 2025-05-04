# 🏠 House Price Prediction Using Regression Models

This project applies **Linear Regression** techniques using `scikit-learn` on a **house prices dataset** (sourced from Kaggle) to predict house prices based on various features.

---

## 📁 Project Structure

- `simple_linear_regression.ipynb`: Uses living area (single variable) to predict house price.
- `multiple_linear_regression.ipynb`: Uses multiple features like bedrooms, living area, and house age to improve prediction accuracy.

---

## 🎯 Objectives

- Predict house prices using both simple and multiple linear regression techniques.
- Apply data preprocessing and variable constraint logic to improve prediction performance.
- Understand the influence of specific house features on price.

---

## 🧪 Models Used

### ✅ 1. **Simple Linear Regression**
- **Independent variable**: `Living Area`
- **Dependent variable**: `Price`
- Objective: Understand basic price correlation with one primary feature.

### ✅ 2. **Multiple Linear Regression**
- **Independent variables**:  
  - Number of Bedrooms  
  - Living Area  
  - House Age (`Old = 2024 - Built Year`)
- **Dependent variable**: `Price`

---

## ⚙️ Data Preparation Notes

### 🔹 Constrained Variables
To reduce model variance and outlier impact, the following constraints were applied:
- **Lot Area**: Only houses with `lot_area ≤ 10,000 sq ft` are included.
- **Waterfront Present**: Only houses with no waterfront (`= 0`) are considered.
- **Renovation Year**: Only houses that have **not** been renovated (`= 0`) are included.
- **Number of Bedrooms**: Range constrained between `2 to 5` bedrooms.
- **Old (House Age)**: Only houses with age ≤ 80 years are considered.
- **Number of Bathrooms**: Limited to houses with ≤ 3 bathrooms.

### 🔹 Excluded or Less Influential Variables
- **Distance from airport**, **latitude**, **longitude**, **number of views**, **condition**, **grade**, **basement-related areas** were not included due to either limited interpretability or high correlation with postal codes.
- **Postal Codes** (`122004` to `122066`): Mostly within the city of **Gurgaon**, hence assumed not to introduce location variance.

---

## 🧩 Assumptions
- **ID** is unique and corresponds to a single house entry.
- Features like `living_area_renov` and `lot_area_renov` were ignored due to lack of clear descriptions.

---

## 🧪 Train-Test Split
A standard `train_test_split()` was used from scikit-learn with `random_state=42` for reproducibility.

---

## 📈 Results & Observations
- Simple linear regression captured basic trends but showed larger error margins.
- Multiple regression provided improved predictions by including more relevant features and reducing the noise via feature constraints.

---

## 📚 Technologies Used
- Python 3
- Pandas
- scikit-learn
- Matplotlib (for visualization)
- Jupyter Notebook

---


## 📌 Acknowledgements
- Dataset sourced from [Kaggle](https://www.kaggle.com/).
- Project inspired by real estate price modeling use-cases.
- For conceptual understanding and code reference related to **Logistic Regression**, refer to this excellent video:
▶️ [Logistic Regression - Code and Concept (YouTube)](https://youtu.be/J_LnPL3Qg70?feature=shared)



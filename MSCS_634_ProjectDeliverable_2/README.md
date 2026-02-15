# MSCS 634 - Project Deliverable 2
## Regression Modeling and Performance Evaluation

---

## 📌 Project Overview

This deliverable focuses on building regression models to predict a target variable using the cleaned Titanic dataset prepared in Deliverable 1. The objective is to apply feature engineering, train multiple regression models, and evaluate their performance using standard regression metrics and cross-validation techniques.

---

## 📊 Dataset Summary

**Dataset Name:** Titanic Passenger Dataset  
**Source:** Kaggle (Public Dataset)  
**Number of Records:** 891  
**Number of Attributes:** 12
**Primary Target Variable (for this deliverable):** Fare

### Key Attributes Used for Modeling:
- Pclass
- Sex
- Age
- SibSp
- Parch
- Embarked
- Engineered features: FamilySize, IsAlone

### Dataset Preparation (from Deliverable 1):
- Missing **Age** values filled using the median.
- Missing **Embarked** values filled using the mode.
- **Cabin** column removed due to excessive missing values.
- Duplicate records removed.
- Dataset inspected for inconsistent or unrealistic values.

---

## 🛠 Feature Engineering

To improve model performance, the following features were created:

### 1. One-Hot Encoding

Converted categorical variables (**Sex** and **Embarked**) into numeric form.

### 2. New Derived Features

- **FamilySize:** Total number of family members aboard.
- **IsAlone:** Binary indicator of whether a passenger was traveling alone.

These features were designed to capture social and travel-related patterns that may influence fare.

---

## 🤖 Regression Models Implemented

Two regression models were developed and compared:

### 1. Linear Regression
- Baseline regression model.
- Assumes a linear relationship between features and the target variable.

### 2. Ridge Regression
- Regularized version of linear regression.
- Helps prevent overfitting by penalizing large coefficients.

---

## 📏 Model Evaluation Metrics

Models were evaluated using:
- **R² (Coefficient of Determination):** Measures how well the model explains variance.
- **Mean Squared Error (MSE):** Average squared difference between predicted and actual values.
- **Root Mean Squared Error (RMSE):** Square root of MSE for interpretability. Provides error interpretation in the same units as the target variable.

### Cross-Validation
- 5-fold cross-validation was used to evaluate model generalization.
- Ensured performance consistency across multiple training splits.

---

## 📊 Key Observations and Insights

- Both models performed similarly in terms of R² and RMSE.
- Ridge Regression produced slightly more stable results due to regularization.
- Passenger class (**Pclass**) was the strongest predictor of fare.
- Engineered features such as **FamilySize** contributed to improved model performance.
- Cross-validation confirmed that the models generalize reasonably well to unseen data.

---

## ⚠️ Challenges Encountered and Solutions

### Challenge 1: Handling Missing Data
- The dataset contained missing values in key attributes.
- **Solution:** Applied median and mode imputation to preserve data distribution.

### Challenge 2: Categorical Variables in Regression
- Regression models require numerical inputs.
- **Solution:** Applied one-hot encoding to convert categorical features.

### Challenge 3: Overfitting Risk
- Linear regression models can overfit when features are correlated.
- **Solution:** Implemented Ridge Regression with regularization and used cross-validation.

### Challenge 4: Pandas Future Warnings
- Warnings appeared due to chained assignment with `inplace=True`.
- **Solution:** Replaced with direct assignment to ensure future compatibility.

---

## 📁 Repository Contents (for this deliverable)

- `MSCS_634_ProjectDeliverable_2.ipynb` – Complete regression implementation with code, comments, and visualizations.
- `README.md` – Project summary, modeling process, insights, and challenges.

---

## ✅ Conclusion

In this deliverable, regression models were successfully developed to predict passenger fare using engineered features from the Titanic dataset. Both Linear and Ridge Regression models showed comparable performance, with Ridge Regression offering more stable results due to regularization. Feature engineering played an important role in improving predictive performance, and cross-validation confirmed that the models generalize effectively. These results provide a solid foundation for more advanced predictive modeling in future deliverables.

---
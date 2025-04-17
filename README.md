# Chronic_Kidney_Disease

# 🧠 Kidney Disease Prediction using Machine Learning

This project predicts whether a person has a risk of chronic kidney disease based on various medical attributes. It includes data preprocessing, exploratory data analysis (EDA), model training with hyperparameter tuning, and integration readiness for web deployment.

---

## 📂 Project Structure


---

## 📊 Dataset

- **Source**: [Kaggle - Kidney Disease Dataset](https://www.kaggle.com/datasets/amanik000/kidney-disease-dataset)
- **Shape**: ~20,000 rows, 25+ features
- **Target Column**: `Target` (Categorical: `"No"` for no risk, `"Yes"` for low/high risk)

---

## 🔍 EDA Highlights

- Handled missing values and inconsistencies.
- Converted all categorical/object-type columns into numerical using:
  - Label Encoding (`Yes`/`No`, `Normal`/`Abnormal`)
  - Manual mapping (`Low`/`Medium`/`High`)
- Correlation heatmap used to analyze feature relationships.
- Balanced the dataset (if necessary).

---

## 🧼 Preprocessing

- Replaced categories using `map()` and `LabelEncoder`.
- Scaled numeric values (if needed).
- Split dataset:
  ```python
  from sklearn.model_selection import train_test_split
  x_train, x_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

## 🤖 Model

- **Algorithm**: `XGBoost Classifier`  
  A fast, high-performance boosting algorithm suitable for structured/tabular data.

- **Why XGBoost?**
  - ✅ Efficient on large and tabular datasets
  - ✅ Supports regularization to reduce overfitting
  - ✅ Natively handles missing values
  - ✅ Works well with imbalanced classes

- **Hyperparameter Tuning**
  - Used `GridSearchCV` for exhaustive search across hyperparameters
  - While it provided optimal results, it was computationally expensive

- **Best Accuracy Achieved**: **~80%**

from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
Accuracy Score

Confusion Matrix

Classification Report (Precision, Recall, F1)

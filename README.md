https://www.kaggle.com/competitions/multiclassificationtask/
# 🩺 Cirrhosis Patient Survival Prediction

This project focuses on predicting the **survival status of cirrhosis patients** (C: censored/alive, CL: censored/alive with liver disease, D: dead) based on their clinical and demographic information. It showcases a machine learning pipeline for multi-class classification, including data preprocessing, model development, and evaluation.

---

## 📂 Dataset

The dataset for this project is from a Kaggle competition: [Cirroz bemorlari omon qolish prognozi](https://www.kaggle.com/competitions/cirroz-bemorlari-omon-qolish-prognozi/). It includes:

-   `train.csv` – training data with features and the `Status` label.
-   `test.csv` – test data for which survival status predictions are required.
-   `sample_submission.csv` – format example for final predictions.

---

## 📊 Project Workflow

### 1. **Initial Data Inspection**
-   Analyzed data types, missing values, and summary statistics.
-   Identified and handled a rare 'Y' class instance in the target variable.

### 2. **Data Preprocessing**
-   Imputed missing categorical features with a 'Missing' category.
-   Imputed missing numerical features with the median.
-   Converted `Age` from days to years.
-   Encoded categorical variables using One-Hot Encoding.
-   Scaled numerical features using `StandardScaler`.

### 3. **Model Building**
Trained and evaluated multiple multi-class classification models using 5-fold Stratified Cross-Validation:
-   ✅ **Logistic Regression**
-   ✅ **Random Forest Classifier**
-   ✅ **LightGBM (LGBMClassifier)**
-   ✅ **XGBoost (XGBClassifier)**
-   ✅ **Support Vector Classifier (SVC)**

### 4. **Evaluation Metric**
-   **LogLoss** (the primary competition metric, lower is better).

---

## 📈 Results

-   **Best model**: Identified the model with the lowest Overall Out-of-Fold (OOF) LogLoss. (Based on your output, this was likely **LightGBM** or **XGBoost**).
-   *(Optional: You can add a specific LogLoss score here once your final runs are complete, e.g., "Achieved an OOF LogLoss of X.XXXX")*


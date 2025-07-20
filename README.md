# 🫀 Cardiovascular Risk Prediction

This project focuses on predicting the **10-year risk of coronary heart disease (CHD)** using clinical and lifestyle-related data. It applies various machine learning models to assess patient data and determine their likelihood of developing CHD within a decade.

---

## 📊 Dataset Overview

- **Total records**: ~4,000 patients
- **Target Variable**: `TenYearCHD` (1 = CHD likely in 10 years, 0 = unlikely)
- **Features Include**:
  - Demographic: Age, Sex, Education
  - Behavioral: Smoking status, Cigarettes per day
  - Medical History: Hypertension, Diabetes, Medications
  - Clinical: Blood pressure (sysBP, diaBP), Cholesterol, BMI, Glucose, Heart Rate

---

## 🛠️ Preprocessing

- Removed missing values via imputation and row-wise dropping (as appropriate)
- Encoded categorical features (like `is_smoking`,`sex`) to binary format
- Normalized/Scaled continuous variables for model input
- Handled outliers using `standardscaler`

---

## 📈 Exploratory Data Analysis (EDA)

Visualizations were created to explore relationships between CHD risk and various features:

- Box plots for `sysBP`, `diaBP`, `BMI`, `glucose`, and `cigsPerDay` by CHD status
- Count plots for categorical features like `is_smoking`, `prevalentHyp`, and `BPMeds`
- Heatmap of correlations among important numerical features
- Pair plot for `age`, `BMI`, `cholesterol`, `sysBP`, and `glucose`

---

## 🤖 Models Used

Three classification models were trained and compared:

| Model               | Description                                  |
|--------------------|----------------------------------------------|
| **Logistic Regression** | Baseline interpretable model               |
| **Random Forest Classifier** | Ensemble method with decision trees     |
| **XGBoost Classifier** | Gradient boosting for improved accuracy    |

---

## 📏 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC Score**

After tuning hyperparameters, we observed performance improvement across all models, especially in recall and F1-score, which are crucial for medical predictions.

---

## 📉 Feature Importance

Random Forest and XGBoost models provided feature importance scores. Top influential features included:
- `age`
- `sysBP` (Systolic Blood Pressure)
- `glucose`
- `BMI`
- `cigsPerDay`

---

## 📌 Key Insights

- Patients with higher **blood pressure**, **glucose levels**, and **BMI** are more likely to develop CHD.
- **Smoking** is a major risk factor, both in terms of behavior and cigarette quantity.
- Lifestyle factors and preventive medication can play a crucial role in lowering risk.

---

## 🧪 Future Improvements

- Implement cross-validation for more robust results
- Explore deep learning with larger datasets
- Deploy a web app for real-time risk prediction

---




## 🧠 Tools & Libraries Used

- Python (Pandas, NumPy)
- Seaborn & Matplotlib
- Plotly for interactive visualizations
- Scikit-learn
- XGBoost

---


---

## 📌 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.


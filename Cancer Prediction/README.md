# Cancer Prediction 
![](CancerPrediction.jpg)

## Project Overview:

The goal of this data science project is to predict whether a patient is likely to be diagnosed with cancer based on medical and lifestyle factors.  
By analyzing attributes such as age, BMI, smoking habits, genetic risk, and physical activity, the project aims to build accurate and interpretable models to assist in early cancer detection and risk assessment.

---

## Data Dictionary:

Below is a detailed description of each feature in the dataset:

| Variable           | Description                                                                 |
|--------------------|------------------------------------------------------------------------------|
| **Age**            | Integer values representing the patient’s age (20–80 years).                |
| **Gender**         | Binary values representing gender (0 = Male, 1 = Female).                   |
| **BMI**            | Continuous values of Body Mass Index (15–40).                               |
| **Smoking**        | Binary indicator of smoking status (0 = No, 1 = Yes).                       |
| **GeneticRisk**    | Categorical variable indicating genetic risk (0 = Low, 1 = Medium, 2 = High).|
| **PhysicalActivity** | Continuous values representing hours per week of physical activity (0–10).|
| **AlcoholIntake**  | Continuous values indicating alcohol units consumed per week (0–5).          |
| **CancerHistory**  | Binary indicator of prior cancer history (0 = No, 1 = Yes).                 |
| **Diagnosis**      | Target variable: 0 = No Cancer, 1 = Cancer.                                 |

---

## Feature Importance Analysis:

Based on feature importance from both **Random Forest** and **XGBoost** models, **CancerHistory** is the most dominant factor influencing cancer prediction.  
Other significant features include **GeneticRisk**, **BMI**, **Smoking**, and **AlcoholIntake**, which also contribute meaningfully to prediction accuracy.  

This indicates that a patient’s medical background, genetic predisposition, and lifestyle habits collectively play key roles in determining cancer likelihood.

| Rank | Feature           | Importance (Top Factors) |
|------|-------------------|---------------------------|
| 1️⃣  | CancerHistory     | Very High                |
| 2️⃣  | GeneticRisk       | High                     |
| 3️⃣  | BMI               | Moderate                 |
| 4️⃣  | Smoking           | Moderate                 |
| 5️⃣  | AlcoholIntake     | Moderate                 |
| 6️⃣  | PhysicalActivity  | Low                      |
| 7️⃣  | Age               | Low                      |
| 8️⃣  | Gender            | Low                      |

---

## Model Performance Summary:

Three classification algorithms were implemented:  
**Logistic Regression**, **Random Forest**, and **XGBoost**.

| Model                | Accuracy | F1-Score | ROC-AUC | Remarks |
|----------------------|-----------|-----------|----------|----------|
| Logistic Regression  | 86.0%     | 0.85      | 0.89     | Good baseline performance |
| Random Forest        | 92.3%     | 0.91      | 0.95     | High accuracy and stable predictions |
| XGBoost Classifier   | **94.3%** | **0.93**  | **0.97** | Best performance and generalization |

The **XGBoost Classifier** achieved the highest performance with an accuracy of **94.3%**, followed by Random Forest at **92.3%** and Logistic Regression at **86%**.  
XGBoost also demonstrated the highest F1-Score and ROC-AUC value, indicating its superior capability in distinguishing between cancer and non-cancer cases.

---

## Conclusion:

- **CancerHistory** has the strongest positive correlation with the target variable, followed by **GeneticRisk** and **Smoking**.  
- Patients with **higher physical activity** levels tend to have a **lower cancer risk**.  
- **XGBoost** outperformed other models and is identified as the most suitable algorithm for this cancer prediction task.  

Overall, the findings suggest that a combination of **medical history**, **genetic predisposition**, and **lifestyle factors** collectively determine a patient’s cancer likelihood.  
With proper validation, this model can contribute to **early cancer detection** and **preventive healthcare analytics**.

---

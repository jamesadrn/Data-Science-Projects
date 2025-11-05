# Telecom Customer Churn Prediction  
![](TelecomCustomerChurnPrediction.jpg)

## Project Overview:
The goal of this project is to predict **customer churn** in a telecommunications company using machine learning.  
By analyzing customer demographics, service subscriptions, and billing information, the project aims to identify customers who are likely to leave the service, helping the company take preventive action to improve retention.

---

## Data Dictionary:

| Variable | Description |
|-----------|-------------|
| **gender** | Gender of the customer (Male / Female). |
| **SeniorCitizen** | Indicates whether the customer is a senior citizen (1 = Yes, 0 = No). |
| **Partner** | Whether the customer has a partner (Yes / No). |
| **Dependents** | Whether the customer has dependents (Yes / No). |
| **tenure** | Number of months the customer has stayed with the company. |
| **PhoneService** | Whether the customer has phone service. |
| **MultipleLines** | Whether the customer has multiple lines. |
| **InternetService** | Type of internet service (DSL, Fiber optic, or None). |
| **OnlineSecurity** | Whether the customer has online security. |
| **OnlineBackup** | Whether the customer has online backup. |
| **DeviceProtection** | Whether the customer has device protection. |
| **TechSupport** | Whether the customer has technical support. |
| **StreamingTV** | Whether the customer has streaming TV service. |
| **StreamingMovies** | Whether the customer has streaming movie service. |
| **Contract** | Type of customer contract (Month-to-month, One year, Two year). |
| **PaperlessBilling** | Indicates if paperless billing is used. |
| **PaymentMethod** | Type of payment method used. |
| **MonthlyCharges** | Monthly charges billed to the customer. |
| **TotalCharges** | Total charges billed to date. |
| **Churn** | Target variable (Yes = Customer left, No = Customer retained). |

---

## Model Performance Summary:

Three classification algorithms were developed:  
**Logistic Regression**, **Support Vector Machine (SVM)**, and **Naive Bayes**.

| Model | Accuracy | ROC-AUC | Remarks |
|--------|-----------|----------|----------|
| **Logistic Regression** | 82.2% | 0.85 | Stable baseline model with good calibration |
| **SVM (RBF Kernel)** | **83.0%** | **0.84** | Best overall performance |
| **Naive Bayes** | 75.3% | 0.82 | Fastest training time |

The **SVM Classifier** achieved the highest accuracy (83%) and competitive ROC-AUC (0.84), outperforming Logistic Regression (82%) and Naive Bayes (75%).  
While Logistic Regression produced smoother probability distributions, SVM delivered stronger classification boundaries and more accurate churn predictions.

---

## Conclusion:

This project focused on predicting customer churn in a telecommunications company using three models — Logistic Regression, Support Vector Machine (SVM), and Naive Bayes. The SVM model achieved the best overall performance with an accuracy of 83% and a ROC-AUC of 0.84, followed by Logistic Regression at 82% and Naive Bayes at 75%.  

From the data analysis, customers who were on month-to-month contracts, had higher monthly charges, and used fiber optic internet were found to be more likely to churn. In contrast, customers with longer tenure and two-year contracts showed significantly lower churn rates. These patterns suggest that billing stability and contract duration play key roles in customer retention.  

Overall, the findings highlight that churn is driven by a mix of service-related and cost-related factors rather than demographic characteristics. The model and insights derived from this project can help telecom companies design better retention strategies, such as offering contract incentives or personalized discounts for at-risk customers.  


--
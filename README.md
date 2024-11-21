# **Predictive Maintenance for Wind Turbines: Generator Failure Detection**

## **Project Overview**

This project focuses on **predictive maintenance** in wind energy, developed in collaboration with **ReneWind**, a company dedicated to optimizing wind energy production using machine learning. The goal is to build and evaluate various **classification models** to predict **generator failures** in wind turbines. Early failure detection will enable timely repairs, reducing overall maintenance costs and improving operational efficiency.

### **Dataset**

- **40 predictors**
- **20,000 observations** in the training set
- **5,000 observations** in the test set

---

## **Objective**

To develop a predictive model that classifies generators as likely to fail (**1**) or not fail (**0**). The predictions will inform decisions to inspect, repair, or replace components, with cost implications:

- **True Positives (TP):** Failures correctly predicted → **Repair Costs**
- **False Negatives (FN):** Failures not detected → **Replacement Costs**
- **False Positives (FP):** Incorrect predictions of failure → **Inspection Costs**

### **Cost Considerations**
- **Replacement costs > Repair costs > Inspection costs**
- The focus is on minimizing **false negatives** due to the high replacement costs.

---

## **Key Steps**

1. **Data Preparation**
   - Ciphered sensor data was preprocessed and analyzed to extract meaningful features.
2. **Model Development**
   - Various classification models were built, including:
     - **XGBoost**
     - **Random Forest**
     - **Logistic Regression**
3. **Model Evaluation**
   - Models were assessed using the following metrics:
     - **Accuracy**
     - **Precision**
     - **Recall**
     - **F1-Score**
     - **Cost Optimization Metrics**
4. **Final Model Selection**
   - The best-performing model was selected based on its ability to minimize overall maintenance costs.

---

## **Best Model: XGBoost**

The **XGBoost model** outperformed other models, achieving the following metrics on the test set:

- **Accuracy:** 0.9890
- **Recall:** 0.8369
- **Precision:** 0.9633
- **F1 Score:** 0.8956

### **Feature Importance and Operational Insights**

#### **Feature Prioritization**
- **V36**: The most important feature. Likely represents critical information (e.g., turbine stress, temperature, or vibration) about potential failures.
- **V14** and **V26**: Significant features that should be closely monitored in operational settings.

#### **Operational Monitoring**
- Features like **V36**, **V14**, and **V26** are likely tied to crucial operational conditions. Ensuring these sensors remain functional is essential to maintain predictive accuracy.

#### **Potential for Feature Reduction**
- Features with low importance (e.g., **V20**, **V17**, **V8**) could be excluded in future iterations to simplify the model and reduce computational costs.

#### **Further Investigation**
- Investigate the nature of **V36** to understand its criticality and inform maintenance priorities.
- Analyze interactions between **V14** and **V26** with other features to gain deeper insights into predictive performance.

---

## **Business Context**

Predictive maintenance in wind energy aims to maximize operational efficiency and reduce downtime by identifying generator issues before failure. This project aligns with **ReneWind's vision** of leveraging data-driven approaches to improve wind turbine reliability and drive cost-effective maintenance.

---

## **Code and Data**

- The **code** for preprocessing, modeling, and evaluation is provided in this repository.
- The **data** used is **ciphered** to maintain confidentiality and is unavailable for public sharing due to proprietary considerations.

---

## **Results**

- The final **XGBoost model** demonstrates high reliability in detecting failures, striking a balance between repair, inspection, and replacement costs.
- **Insights gained** from feature importance are directly applicable to enhancing maintenance strategies in wind energy.

---


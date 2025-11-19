# BT4012 Group 7 — Insurance Fraud Detection

This repository contains the workflow for the BT4012 Fraud Analytics group project. The objective is to detect fraudulent vehicle-insurance claims using machine learning techniques applied to historical demographic, policy, vehicle, and claim-submission data.

The project includes data cleaning, feature engineering, model training, hyperparameter tuning with Optuna, and business-oriented threshold optimisation. The final selected model was **XGBoost**, which achieved the strongest validation ROC-AUC and highest net financial benefit.

---

## Project Structure

```
BT4012-Group-7/
│── BT4012_Group07_EDA.ipynb
│── BT4012_Group07_Data_Preparation.ipynb
│── BT4012_Group07_Correlation.ipynb
│── BT4012_Group07_Logistic_Regression.ipynb
│── BT4012_Group07_Random_Forest.ipynb
│── BT4012_Group07_XGBoost.ipynb
│── BT4012_Group07_MLP.ipynb
│── final_dataset.csv
│── fraud_oracle.csv
│── requirements.txt
│── README.md
```
Each notebook corresponds to a specific stage of the pipeline for full reproducibility.

---

## Installation

To install dependencies:
pip install -r requirements.txt


---

## How to Run the Project

Run the notebooks in this order:

1. **BT4012_Group07_Data_Preparation.ipynb**  
2. **BT4012_Group07_EDA.ipynb**  
3. **Modelling notebooks:**  
   - Logistic Regression  
   - Random Forest  
   - XGBoost  
   - MLP
4. **BT4012_Group07_Correlation.ipynb**

Each modelling notebook includes stratified splitting, Optuna tuning, ROC-AUC evaluation, and business-centric threshold optimisation.
The XGBoost notebook additionally includes the final test-set evaluation.

---

## Results Summary

| Model | Validation ROC-AUC | Net Benefit |
|-------|---------------------|-------------|
| **XGBoost** | **0.8253** | **$1,050** |
| Random Forest | 0.7984 | $1,045 |
| MLP | 0.7935 | $951 |
| Logistic Regression | 0.7634 | $901 |

**Final Test Performance (XGBoost, business-optimal threshold = 0.10):**
- ROC-AUC: 0.8285  
- Fraud recall: 0.97  
- Precision: 0.13  
- Net benefit: $2,226  

---

## Key Engineered Features

- DaysClaimProcessingDelay  
- InvalidClaimProcessingDelay  
- DaysAccidentToClaimDelay  
- DeductibleVehiclePriceRatio  

---

## Team Members

- Pang Zi Ying, Petrine — A0257268R  
- Khoo Hui Qian — A0259528N  
- Delia Tan Hwee Cheng — A0283302N  
- Cai Yu Shi — A0258328W  




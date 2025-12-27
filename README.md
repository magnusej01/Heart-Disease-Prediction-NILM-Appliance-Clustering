# Heart-Disease-Prediction-NILM-Appliance-Clustering

# Supervised and Unsupervised Machine Learning:
## Heart Disease Prediction and NILM Appliance Clustering

## Overview

This project applies both supervised and unsupervised machine learning to two real world problems. The first task predicts heart disease using Logistic Regression on the Cleveland Heart Disease dataset. The second task applies K means clustering with and without PCA to group appliance level power events in a Non Intrusive Load Monitoring (NILM) setting using the UK DALE dataset.

The goal is to balance accuracy, interpretability, fairness, and responsible AI practice across both workflows.

This project was completed as part of the course IAI4100 Introduction to AI.

---

## Objectives

1. Build an interpretable supervised model to predict heart disease  
2. Apply structured preprocessing and feature engineering  
3. Evaluate medical classification performance using accuracy, precision, recall, F1 and ROC AUC  
4. Design an unsupervised NILM pipeline for grouping electrical appliance events  
5. Compare K means with and without PCA dimensionality reduction  
6. Reflect on fairness, ethics, and sustainability in AI modelling  

---

## Part 1: Supervised Learning  
### Heart Disease Prediction

### Dataset

Cleveland Heart Disease dataset  
303 patient records  
13 clinical input features  
Binary target: disease or no disease  

### Preprocessing

One hot encoding of categorical variables  
Variance threshold filtering  
Correlation filtering to reduce multicollinearity  
Standard scaling of continuous features  
Stratified train and test split  

These steps produced a refined set of 17 informative predictors aligned with clinical meaning.

### Model

Logistic Regression was chosen because it is:

• interpretable  
• probabilistic  
• appropriate for binary outcomes  

### Performance

Accuracy: 0.87  
F1 Score: 0.87  
ROC AUC: 0.96  

The model detected most positive cases while keeping false negatives low, which is important in healthcare risk prediction.

### Key Insight

Logistic Regression remains competitive while staying transparent, which supports medical decision making where explainability matters.

---

## Part 2: Unsupervised Learning  
### NILM Appliance Event Clustering

### Problem

Recover appliance level activity from whole-home electricity signals without labels.

Dataset: UK DALE, House 1  
Cadence: 6 seconds  
On threshold: 5W  

Short gaps were forward filled and long gaps set to zero to ensure continuity.

### Pipeline

1. Preprocessing and event detection  
2. Feature engineering  
3. K means clustering  
4. PCA dimensionality reduction variant  
5. Evaluation using accuracy and macro F1  

Engineered features included:

Amp_W  
Duration_s  
Energy_Wh  
Hour_of_day  

### Evaluation

Baseline K means  
Accuracy: 0.779  
Macro F1: 0.286  

PCA + K means  
Accuracy: 0.779  
Macro F1: 0.302  

PCA improved separability for some appliances but reduced it for others, showing the trade off between variance preservation and predictive alignment.

---

## Technology and Tools

Python  
Scikit Learn  
Pandas  
NumPy  
Matplotlib  
Seaborn  

Logistic Regression  
K Means Clustering  
Principal Component Analysis  

---

## Learning Outcomes

Through this project I strengthened my skills in:

• building interpretable medical prediction models  
• applying structured preprocessing and feature filtering  
• evaluating models beyond accuracy  
• designing unsupervised clustering workflows  
• understanding dimensionality reduction trade offs  
• reflecting on fairness, reproducibility, and responsible AI  

---


## Ethical and Sustainability Reflection

The project includes explicit consideration of:

• fairness across gender distribution  
• interpretability in medical prediction  
• transparency through documented preprocessing  
• computational efficiency  
• reproducibility through fixed seeds and logged configuration  

---

## Disclaimer

This project is created for academic and learning purposes.


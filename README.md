# heart-disease-logistic-regression

# Heart Disease Prediction Using Logistic Regression

## Overview
This project explores predicting heart disease severity using clinical risk factors from a public heart disease dataset. The goal is to build a model that can identify patients who may be at risk and estimate the severity of their condition. Early prediction of heart disease can support timely diagnosis and treatment.

This repository contains the **logistic regression implementation and analysis** used in the project.

## Dataset
The data comes from a public Kaggle heart disease dataset containing 14 medical attributes used to predict heart disease risk.

Key features include:
- Age
- Sex
- Chest pain type
- Resting blood pressure
- Serum cholesterol
- Fasting blood sugar
- Resting electrocardiographic results
- Maximum heart rate achieved
- Exercise-induced angina
- ST depression induced by exercise relative to rest (oldpeak)
- Slope of the peak exercise ST segment
- Number of major vessels colored by fluoroscopy (ca)
- Thalassemia (thal)

The target variable **num** represents heart disease severity:

| Value | Meaning |
|------|--------|
| 0 | No heart disease |
| 1–4 | Increasing severity of heart disease |

## Methodology
The learning task is formulated as a **classification problem**.

Steps in the modeling pipeline:

1. Data preprocessing and cleaning  
2. Train/test split (75% training, 25% testing)  
3. Logistic regression model training  
4. Addressing class imbalance using **upsampling**  
5. Model evaluation using accuracy, precision, recall, and confusion matrix

## Key Considerations
The dataset contains **class imbalance**, particularly for severe heart disease cases. This caused the baseline model to struggle with detecting high-risk patients.

To improve detection of rare cases, **upsampling** was applied during training.

In healthcare prediction tasks, **recall is often prioritized over precision**, since missing a true case (false negative) can have serious consequences.

## Results
The baseline logistic regression model achieved approximately **50% accuracy** and had difficulty identifying severe cases.

After addressing class imbalance:

- Recall for the most severe class improved from **0.00 to 0.80**
- The model became less biased toward predicting only majority classes
- Detection of higher-risk patients improved

Although the model still struggles with the most severe cases due to limited data, performance improved compared to the initial baseline.



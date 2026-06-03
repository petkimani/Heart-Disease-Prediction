# Project Overview

This project builds a full clinical prediction pipeline for heart disease using the UCI Heart Disease dataset. It covers
exploratory analysis, outlier handling, categorical encoding, feature correlation analysis, and Random Forest
classification — deployed via a Streamlit web app for real-time patient risk scoring.

# Dataset Summary

918 patients, 11 features, target class breakdown, split between numerical and categorical features.

# Data Cleanin

Three dedicated steps: Z-score outlier removal, RestingBP zero-row deletion, and the group-specific cholesterol median imputation (with explanation of why group-specific matters clinically).

# EDA

4 tabbed charts: categorical distributions (chest pain types vs diagnosis), age histogram, sex vs heart disease, and a chest pain type doughnut chart. Each with detailed interpretation. Key clinical insight: ASY (asymptomatic) patients paradoxically have the highest heart disease rates.

# Correlation Heatmap

Interactive heatmap with colour coding by correlation strength, plus 6 call-out boxes explaining the most important relationships — ST_Slope_Up being the strongest negative predictor (−0.59), and ExerciseAngina_Y the strongest positive one (+0.49).

# Feature Importance

Horizontal bar chart with the top 10 features, red-highlighted top 6 used in the Streamlit app, with clinical interpretation of each group.

# Model Training

Configuration, code, and a note that no max_depth was set (a potential overfitting risk on ~860 rows).

# Confusion Matrix

In a medical context, False Negatives (missed heart disease) are clinically far more dangerous than False Positives (unnecessary further tests). The model should therefore be evaluated primarily on Recall for class 1 (heart disease present).

# Streamlit Deployment

Covers the 6-feature app UI, caching strategy, and design rationale.

# Recommendations

GridSearchCV tuning, class imbalance handling, ROC/PR curves, and SHAP explainability.

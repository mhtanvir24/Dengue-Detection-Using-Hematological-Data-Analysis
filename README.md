# Dengue-Detection-Using-Hematological-Data-Analysis

*Project Overview-
This project analyzes a hematological (blood test) dataset of 1,523 dengue patients to understand how routine Complete Blood Count (CBC) values differ between dengue-positive and dengue-negative cases, and to build a machine learning model that predicts dengue infection from those values.

Dengue is usually confirmed with NS1 or IgM/IgG antibody tests, which are accurate but often expensive or unavailable outside major hospitals. A CBC test, on the other hand, is cheap, fast, and available almost everywhere. Since dengue infection is known to change blood parameters such as platelet count and white blood cell composition, this project was developed to explore whether those routine, low-cost values can support early dengue screening — combining statistical analysis with a supervised classification model.

*Objectives-
Perform comprehensive exploratory data analysis (EDA) on the hematological dataset (boxplots, histograms, count plots, correlation heatmap).
Run independent-sample t-tests to statistically identify which blood parameters differ significantly between dengue-positive and dengue-negative patients.
Clean and preprocess the dataset (handle missing values, encode categorical variables, detect/interpret outliers).
Train and evaluate a HistGradientBoostingClassifier to predict dengue result from CBC parameters.
Report model performance using accuracy, ROC-AUC, and a confusion matrix, and discuss its practical usefulness and limitations.

*Problem Statement
Dengue fever is a common mosquito-borne disease that spreads quickly in tropical countries like Bangladesh and can become severe or life-threatening without early diagnosis. Confirmatory dengue tests are not always accessible in small hospitals or rural clinics, while CBC tests are routinely performed almost everywhere. However, the changes a CBC shows during dengue infection are not always easy for non-specialists to interpret correctly and consistently. This project addresses that gap by statistically identifying which CBC parameters are meaningfully associated with dengue and using them to build a simple predictive model that could support faster, low-cost initial screening.

*Key Features
Data cleaning & preprocessing — missing-value handling, dropping incomplete Gender records, one-hot encoding of categorical fields.
Exploratory Data Analysis — dengue result distribution, gender vs. result breakdown, age distribution of positive cases, and boxplots for 14 hematological parameters plus Age.
Outlier identification — IQR-based outlier detection per numeric column, with outliers retained (not removed) to preserve genuine clinical variation.
Correlation analysis — full correlation heatmap across all blood parameters and demographic variables.
Statistical inference — Welch's independent-sample t-tests comparing every numeric variable between positive and negative groups, with significance flags at p < 0.05.
Machine learning model — HistGradientBoostingClassifier trained on an 80/20 stratified split, tuned with 500 iterations, learning rate 0.05, max depth 6, and L2 regularization 0.1.
Model evaluation — accuracy, ROC-AUC, and confusion matrix reporting, achieving 74.34% accuracy and 0.6719 ROC-AUC.

*Limitation
The limitation of this project is that it is built on a limited dataset with restricted features, leading to only moderate model performance and reliability. Due to the absence of important real-world factors, lack of advanced optimization and model comparison, and no external validation, the model’s ability to generalize and be used in actual clinical settings remains constrained.

**Reference:
“A comprehensive hematological dataset for dengue incidence in Bangladesh”
Available: https://www.sciencedirect.com/science/article/pii/S2352340925003944

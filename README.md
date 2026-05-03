Project Overview
This project is part of the AI/ML Internship Week 2, focusing on data analysis using NumPy and Pandas.
The objective is to explore the Titanic dataset, clean and preprocess the data, engineer meaningful features, and extract key insights related to passenger survival.

Dataset Information
Dataset: Titanic Dataset
Total Records: 891 passengers
Total Features: 12 original columns
Missing Values:
Age: 177 (~19.86%)
Cabin: 687 (~77.1%)
Embarked: 2

Tools & Libraries Used
Python 
NumPy
Pandas
Matplotlib
Seaborn
Scikit-learn
Data Cleaning & Preprocessing
Filled missing Age using group-based median (Pclass + Sex)
Filled Embarked with mode
Created has_cabin feature and dropped original Cabin column
Handled Fare outliers using winsorization (capping)

Feature Engineering
Created 7 new features:
family_size
is_alone
fare_per_person
title (extracted from Name)
age_group
fare_bin
has_cabin

These features improved both interpretability and model performance readiness.
Key Survival Insights
Top 3 Findings:
1. Gender Impact
Female survival rate ≈ 74%
Male survival rate ≈ 19%
Gender is the strongest predictor of survival
2. Passenger Class Impact
1st Class: 63% survival
2nd Class: 47% survival
3rd Class: 24% survival
Higher class passengers had significantly better survival chances
3. Combined Effect (Pclass + Sex)
1st Class Females: 96.8% survival (highest)
3rd Class Males: 13.5% survival (lowest)

Visualization Dashboard
The project includes a 6-chart EDA dashboard, covering:
Survival rate by passenger class
Age distribution (survivors vs non-survivors)
Fare distribution by class
Heatmap (Pclass vs Sex survival rate)
Family size vs survival
Title-based survival patterns

Dashboard Preview:
Correlation Insights
Top features correlated with survival:
sex_encoded → 0.54
title_Mrs → 0.33
title_Miss → 0.32
has_cabin → 0.31
Fare → 0.27

ML Feature Selection
Recommended features for model training:
Sex (encoded)
Pclass
Fare
Age
Family Size
Title features

NumPy Analysis Insights
Standardization verified: mean ≈ 0, std ≈ 1
Survivors had higher average fare than non-survivors
Suggests economic/class advantage played a key role in survival
Repository Contents
titanic_analysis.ipynb → Complete notebook
titanic_cleaned.csv → Final processed dataset
titanic_dashboard.png → Visualization dashboard

Reflection
This project enhanced my understanding of:
Data cleaning and preprocessing techniques
Feature engineering strategies
Data visualization for insight extraction
Handling real-world messy datasets

The most challenging part was feature engineering and encoding, especially extracting meaningful patterns from text-based columns like passenger names.

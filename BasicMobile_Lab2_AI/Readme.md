pima-diabetes-ai-lab

This repository contains the AI practice assignments performed in the “Basic Mobile Lab 2” course at Dankook University. The lab focuses on applying machine learning techniques to the PIMA Indians Diabetes Dataset, offering hands-on experience with linear regression and decision trees using scikit-learn.



Course Overview
* Course Title: Basic Mobile Lab II – Artificial Intelligence
* Instructor: Kim Jeong-hun (AI Engineer, MEDiThings)
* Department: Mobile System Engineering, Dankook University
* Semester: 2024, 2nd Semester

The course provides foundational knowledge and practical skills in machine learning using Python. It emphasizes:
* Understanding supervised learning (regression and classification)
* Using scikit-learn for model development
* Applying ML models to real-world datasets (e.g., PIMA Diabetes dataset)
* Using Google Colab as a research-focused development environment



Basic Theory

Machine Learning Fundamentals
* Supervised Learning: Predicts output (label y) from input variables (X), e.g.:
y = f(X) + ε
    where:
    * f is the true relationship between features and label
    * ε is irreducible error (data noise)

* Regression vs Classification:
    * Regression: Predict continuous values (e.g., blood glucose level)
    * Classification: Predict discrete labels (e.g., diabetes: yes/no)



Scikit-Learn Usage

scikit-learn allows you to:
* Import ML models
* Instantiate the model
* Fit the model to data
* Predict outcomes

Its simplified API enables fast experimentation and is consistent across models.



Implemented Tasks

Task 1 – Linear Regression
* Goal: Predict a continuous value using LinearRegression
* Practice: Feature-target mapping, model fitting, visualization of results

Task 2 – Decision Tree (Regression)
* Goal: Compare decision tree regression to linear regression
* Emphasis on tree depth, overfitting prevention, and model interpretability

Task 3 – Decision Tree (Classification)
* Goal: Classify individuals as diabetic or non-diabetic
* Evaluation: Accuracy, confusion matrix, precision/recall



Environment
* Python 3.10+
* Google Colaboratory
* Libraries: pandas, numpy, scikit-learn, matplotlib, seaborn



Learning Objectives
Through these tasks, students learned:
* How to define an ML problem (regression vs classification)
* How to prepare and load structured data
* How to fit simple ML models using scikit-learn
* How to interpret the results (e.g., model accuracy, feature importance)



References
* PIMA Indians Diabetes Dataset (UCI)
* ISLR (Introduction to Statistical Learning)
* scikit-learn Documentation: https://scikit-learn.org/
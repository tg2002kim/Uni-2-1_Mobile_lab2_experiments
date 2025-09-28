Dankook University, 2nd Year 2nd Semester (Fall 2024)

# Basic Mobile Lab II – AI & ECG Signal Experiments

This repository collects all project and assignment outcomes from the course Basic Mobile Lab II (기초모바일실험), offered by the Department of Mobile System Engineering, Dankook University, during the second semester of the second year (2024).
It includes hands-on experiments in both **AI-based data analysis** and **ECG signal acquisition with mobile visualization** using Arduino and MIT App Inventor.

---

## Course Overview

- **Course Title**: Basic Mobile Lab II
- **Department**: Mobile System Engineering, Dankook University
- **Semester**: 2nd Semester, 2024
- **Instructor**: Kim Jeong-hun (AI Engineer, MEDiThings)

The course consists of two major experimental tracks:
1. **AI Lab using Python & scikit-learn**
2. **ECG Acquisition & Visualization using Arduino and Mobile App**

---

## AI Experiments on PIMA Diabetes Dataset

### Overview

The AI lab focused on exploring core supervised learning models on a real-world dataset – the **PIMA Indians Diabetes Dataset**. The students implemented regression and classification tasks using **scikit-learn** in Python, with Google Colab as the development environment.

### Learning Goals

- Understand the difference between regression and classification.
- Learn how to use scikit-learn for modeling.
- Explore feature-target relationships and model performance.
- Evaluate models using metrics such as MSE, accuracy, and confusion matrix.

### Theory Recap

#### 🔸 Supervised Learning

Predicts an output \( y \) based on input \( X \), formulated as:  
`y = f(X) + ε`  
Where:
- `f(X)`: true relationship between input and output
- `ε`: irreducible noise

#### 🔸 Types
- **Regression**: Continuous output prediction (e.g., glucose level)
- **Classification**: Discrete label prediction (e.g., diabetic or not)

#### 🔸 scikit-learn API Flow
```python
from sklearn.model import ModelType
model = ModelType(...)
model.fit(X_train, y_train)
pred = model.predict(X_test)

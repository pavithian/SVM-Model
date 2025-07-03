# 🤖 Task 7 – Support Vector Machine (SVM) Classification

In this task, we used the **Breast Cancer Wisconsin dataset** to classify tumors as **benign** or **malignant** using Support Vector Machines (SVM).  
We compared two kernels: **Linear** and **RBF (Radial Basis Function)**.

---

## 📦 Dataset Overview

- **Dataset**: Scikit-learn built-in Breast Cancer dataset
- **Target**: Binary (0 = malignant, 1 = benign)
- **Features**: 30 numeric columns (radius, texture, perimeter, area, etc.)

---

## ✅ Steps Performed

### 🔹 1. Data Preprocessing
- Loaded dataset using `load_breast_cancer()`
- Standardized features using `StandardScaler`
- Split into training and test sets (70/30)

### 🔹 2. Model Training
- Trained SVM with `kernel='linear'`
- Trained SVM with `kernel='rbf'` (with `C=1.0`, `gamma='scale'`)

### 🔹 3. Evaluation
- Accuracy score
- Confusion matrix
- Classification report (precision, recall, f1)
- 5-fold cross-validation scores

### 🔹 4. Optional Visualization
- Decision boundary plotted using first two features
- Contour plot + scatter plot of classes

---

## 📊 Results Summary

| Model         | Accuracy | 5-Fold CV Score |
|---------------|----------|-----------------|
| SVM Linear    | 97.66%   | 97.01%          |
| SVM RBF       | 97.07%   | 97.36%          |

✅ **RBF SVM** slightly outperformed on CV score.  
✅ **Linear SVM** was slightly more interpretable.

---

## 🔍 Interview Q&A – SVM

### Q1. What is SVM?
SVM is a supervised ML algorithm that finds the **optimal hyperplane** to separate classes with **maximum margin**.

### Q2. What is a kernel function?
Kernel function maps low-dimensional data into higher dimensions to make it linearly separable.

### Q3. What are common kernel types?
- `linear`
- `rbf` (Gaussian)
- `poly` (polynomial)
- `sigmoid`

### Q4. What is the role of C and gamma?
- **C** controls tradeoff between smooth decision boundary and classifying training points correctly.
- **Gamma** defines how far the influence of a single training point reaches.

### Q5. When to use RBF vs Linear?
- Use **linear** when data is already linearly separable.
- Use **RBF** when classes are not linearly separable.

### Q6. Does SVM support multi-class classification?
Yes, using strategies like **One-vs-One (OvO)** or **One-vs-Rest (OvR)**.

### Q7. What is soft margin SVM?
Allows some misclassifications by introducing slack variables to handle noise in data.

### Q8. Is SVM sensitive to feature scaling?
✅ YES. SVM **requires normalization** of features for accurate distance-based margin computation.

---

## 📁 Folder Contents

task-7-svm-classification/
├── task7_svm_classification.ipynb
├── decision_boundary.png (optional)
└── README.md

yaml
Copy
Edit

---

## 👨‍💻 Author

**Pavithiran**  
B.Tech – Artificial Intelligence and Machine Learning  
Sri Shakthi Institute of Engineering and Technology, Coimbatore

---

## 📎 License



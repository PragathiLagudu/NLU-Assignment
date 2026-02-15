# 📰 Text Classification of BBC News Articles (Sports vs Politics)

## 📌 Project Overview

This project presents a supervised machine learning approach for **binary text classification**, where news articles are categorized into **Sports** and **Politics** classes. The system combines classical Natural Language Processing (NLP) techniques with statistical feature extraction using **TF-IDF**, followed by model training using multiple machine learning algorithms.

The primary objective of the study is to design a reliable classifier, apply proper preprocessing, prevent data leakage, and evaluate model performance using robust validation techniques.

---

## 📂 Dataset

The dataset used in this project is derived from the **BBC News Corpus**, a widely recognized benchmark dataset in NLP research. The original corpus contains multiple categories; however, for this task, only two classes were selected:

- **Politics → Label 0**
- **Sports → Label 1**

This filtering enables focused evaluation of binary classification performance.

---

## 🧹 Data Preprocessing

To improve model generalization and reduce noise, a structured preprocessing pipeline was implemented. The following steps were applied:

✔ Conversion to lowercase  
✔ Removal of numbers and punctuation  
✔ Stopword removal  
✔ Lemmatization  
✔ Whitespace normalization  
✔ Duplicate document removal  
✔ Document length filtering (50–400 words)

These transformations ensure consistent textual representation and mitigate memorization effects.

---

## 🔢 Feature Representation

Text documents were converted into numerical vectors using **TF-IDF (Term Frequency–Inverse Document Frequency)**. This representation emphasizes informative words while reducing the impact of overly frequent terms.

Vectorizer configuration:

- Unigram features only  
- Controlled vocabulary size  
- Minimum and maximum document frequency thresholds  
- Sublinear term-frequency scaling  

The vectorizer was fitted exclusively on training data to prevent data leakage.

---

## 🤖 Machine Learning Models

Three supervised learning algorithms were evaluated:

1. **Random Forest Classifier**
2. **Support Vector Machine (LinearSVC)**
3. **Logistic Regression**

These models were chosen due to their effectiveness in high-dimensional text classification tasks.

---

## 📊 Results

All classifiers achieved strong performance, reflecting the structured nature of the dataset and the effectiveness of TF-IDF features.

### ✅ Accuracy Comparison

![Accuracy Comparison](Results/accuracy_plot.png)

---

### ✅ Confusion Matrices

**Random Forest**

![Random Forest Confusion Matrix](Results/rf_cm.png)

**Support Vector Machine (SVM)**

![SVM Confusion Matrix](Results/svm_cm.png)

**Logistic Regression**

![Logistic Regression Confusion Matrix](Results/lr_cm.png)

---

## 🔁 Cross-Validation

Five-fold cross-validation was conducted to validate model stability and reliability.

- Mean Accuracy ≈ **99.5%**
- Minimal variation across folds

This confirms that model performance is not dependent on a particular data split.

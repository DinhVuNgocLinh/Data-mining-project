# Obesity Risk Prediction Using Data Mining

## 👥 Team Members – Group A

* Phạm Vũ Tuyết Anh
* Đinh Thị Thanh Hằng
* Lê Thị Tuyết My
* Đinh Vũ Ngọc Linh

---

## 📚 Table of Contents

1. [Overview](#i-overview)
2. [Objectives](#ii-objectives)
3. [Dataset](#iii-dataset)
4. [Methodology](#iv-methodology)

   * [Preprocessing](#1-preprocessing)
   * [Modeling](#2-modeling)
   * [Evaluation](#3-evaluation)
5. [Results](#v-results)
6. [Key Learnings](#vi-key-learnings)
7. [Future Work](#vii-future-work)
8. [References](#references)

---

## I. Overview

Obesity is a global health issue with multifactorial causes including genetics, behavior, environment, and lifestyle. This project uses machine learning techniques to analyze and predict **obesity risk levels** based on personal and lifestyle attributes.

---

## II. Objectives

* Build a **classification/prediction framework** to determine obesity risk.
* Explore multiple **data mining algorithms**.
* Improve model performance through **advanced preprocessing** and **ensemble methods**.
* Evaluate performance using statistical and classification metrics.

---

## III. Dataset

* **Source**: [Obesity Level Dataset – Kaggle](https://www.kaggle.com/datasets/jpkochar/obesity-risk-dataset)
* **Records**: 20,757 instances
* **Features**: 16 input variables (age, gender, height, weight, habits, etc.)
* **Target**: Obesity level class (`0be1dad`, later renamed to `class`)

---

## IV. Methodology

### 1. Preprocessing

* Removed duplicates & outliers (post-transformation)
* Categorical encoding (Label & One-hot)
* Power Transformation for normalization
* Feature selection via Random Forest importance

### 2. Modeling

* Implemented models in **Java** using **Weka API**
* Models built:

  * **Single models**: ZeroR, J48 (Decision Tree), SMO (SVM), Naive Bayes, KNN
  * **Ensemble models**: Random Forest, Gradient Boosting, Voting Classifier
  * **Deep learning**: Neural Network

### 3. Evaluation

* Metrics: Accuracy, Precision, Recall, F1-Score, MAE, RMSE, ROC-AUC, PRC
* Compared **baseline**, **individual models**, and **ensembles**

---

## V. Results

| Model                 | Accuracy   | F1-Score | Run Time |
| --------------------- | ---------- | -------- | -------- |
| ZeroR (baseline)      | 39.29%     | -        | <1s      |
| J48 (old dataset)     | 91.75%     | 0.681    | 1s       |
| J48 (improved)        | 93.19%     | 0.931    | 1s       |
| Random Forest         | 93.60%     | 0.936    | 4s       |
| Gradient Boosting     | 93.08%     | 0.931    | 2s       |
| Neural Network        | 91.14%     | 0.911    | 16s      |
| **Voting Classifier** | **94.12%** | **0.94** | 10s      |

### Best Model: **Voting Classifier**

* Highest accuracy and consistency across classes
* Strong performance on precision, recall, F1, and ROC-AUC
* Slight tradeoff in runtime

---

## VI. Key Learnings

* Mastered **end-to-end data mining pipeline**: from cleaning to modeling
* Practiced **ensemble learning techniques** and **model evaluation**
* Understood **bias-variance tradeoffs**, especially in medical data contexts
* Collaborated effectively using structured planning and task delegation

---

## VII. Future Work

* Integrate **deep learning frameworks** (e.g., TensorFlow, PyTorch)
* Use **feature engineering** to enrich inputs (e.g., BMI)
* Deploy model as a **web app** or **REST API** for real-world testing
* Investigate model robustness with real-world, noisy datasets

---

## References

* Dataset: [https://www.kaggle.com/datasets/jpkochar/obesity-risk-dataset](https://www.kaggle.com/datasets/jpkochar/obesity-risk-dataset)
* Weka Documentation: [https://waikato.github.io/weka-wiki/](https://waikato.github.io/weka-wiki/)
* YouTube Tutorials: [Weka Java API](https://www.youtube.com/playlist?list=PLea0WJq13cnBVfsPVNyRAus2NK-KhCuzJ)

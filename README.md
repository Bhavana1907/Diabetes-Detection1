# ⚕️Healthcare Predictive Analytics (Data Analytics)

Predicting Diabetes using ML classifiers

# Diabetes Prediction using SMOTE and GAN-based Data Balancing

This project aims to predict whether a patient is diabetic based on a range of health metrics, using the PIMA Diabetes dataset. It addresses the challenge of class imbalance using *SMOTE (Synthetic Minority Over-sampling Technique)* and \*GAN (Gen# ⚕️ Healthcare Predictive Analytics (Data Analytics)
Predicting Diabetes using ML classifiers

# 🔍 Diabetes Prediction using SMOTE and GAN-based Data Balancing

This project aims to predict whether a patient is diabetic based on a range of health metrics, using the PIMA Diabetes dataset. It addresses the challenge of class imbalance using *SMOTE (Synthetic Minority Over-sampling Technique)* and *GAN (Generative Adversarial Networks)* for synthetic data generation. Multiple machine learning models including \*XGBoost, \*\*Random Forest, and \**Support Vector Machine (SVM)* are evaluated.

---

## 📊 Dataset Description

* *Source*: [Kaggle - Diabetes Dataset](https://www.kaggle.com/johndasilva/diabetes)
* *Samples*: 768 records
* *Features*: 9 input features, 1 target (Outcome)

  * Outcome: 0 = Non-diabetic, 1 = Diabetic
* No missing values, but zero values in features like BMI and Skin Thickness were replaced with the mean of the column.

---

## 🔧 Data Preprocessing

1. Replaced zero or missing values using column mean or median.
2. Normalized features to ensure consistent scale.
3. Cleaned column names.
4. Visualized feature distributions with histograms.

---

## ⚖ Data Balancing Techniques

*Problem*: The dataset is imbalanced with more non-diabetic (class 0) than diabetic (class 1) samples.

* *SMOTE*: Interpolates between existing minority class samples to generate synthetic data.
* *GAN*: Uses adversarial networks to generate highly realistic synthetic samples.

*Visuals*:

* Feature distributions before and after balancing.
* Performance comparison of models using SMOTE vs GAN.

---

## 🛠 Technologies Used

* *Python 3.8+*
* *Libraries*:

  * 🐍 pandas, numpy
  * 🤖 scikit-learn, imbalanced-learn
  * 📈 matplotlib, seaborn

---

## 🔢 Algorithms and Models

### 1️⃣ SMOTE (Synthetic Minority Over-sampling Technique)

* Interpolates new synthetic samples using KNN.
* Enhances minority class representation.

### 2️⃣ GAN (Generative Adversarial Networks)

* Composed of Generator and Discriminator neural networks.
* Trains to generate highly realistic data via adversarial learning.

### 3️⃣ XGBoost

* Boosted decision trees with regularization.
* *Accuracy*:

  * SMOTE: 78.5%
  * GAN: 82.5%

### 4️⃣ Random Forest

* Ensemble of decision trees using bagging.
* *Accuracy* with GAN: 80.5%

### 5️⃣ Support Vector Machine (SVM)

* Constructs maximum-margin hyperplane.
* *Accuracy* with GAN: 81.0%erative Adversarial Networks)\* for synthetic data generation. Multiple machine learning models including \*XGBoost, \*\*Random Forest, and \**Support Vector Machine (SVM)* are evaluated.

---

  ## 🔚 SMOTE vs GAN: Comparative Analysis

| **Aspect**                  | **SMOTE**                                                | **GAN**                                                     |
|----------------------------|-----------------------------------------------------------|-------------------------------------------------------------|
| **Synthetic Data Quality** | Generates linear interpolations using nearest neighbors   | Generates complex, realistic samples via neural networks    |
| **Computational Cost**     | Low — fast and easy to compute                            | High — requires more time and resources                     |
| **Overfitting Risk**       | Moderate                                                  | Lower due to better data diversity                          |
| **Implementation Ease**    | Easy — available via `imbalanced-learn`                   | Moderate — requires GAN architecture and tuning             |
| **Best Performing Model**  | XGBoost: **78.5%** accuracy                               | XGBoost: **82.5%** accuracy                                 |
| **Overall Accuracy Gain**  | Moderate improvement over baseline                        | Significant improvement across all models                   |

### 📌 Summary

- **SMOTE** is a straightforward, easy-to-use technique for oversampling that works well with traditional ML models.
- **GAN** generates more realistic and varied data, resulting in **higher accuracy**, especially with advanced models.
- In this project, **GAN-based augmentation consistently outperformed SMOTE**, particularly for **XGBoost, SVM, and Random Forest**.


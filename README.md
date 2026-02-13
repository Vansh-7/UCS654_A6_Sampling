# Credit Card Fraud Detection: Sampling Impact Analysis
---

## 📌 Project Overview
This project focuses on the systematic evaluation of different **sampling techniques** to address class imbalance in a credit card transaction dataset. In real-world fraud detection, the minority class (fraud) is often overshadowed by the majority class (genuine), leading to biased models. This study demonstrates how balancing and sampling influence the performance of five distinct machine learning models.

---

## 🛠 Methodology

### 1. Data Preprocessing & Balancing
The original dataset was highly imbalanced, containing significantly fewer fraud cases than genuine ones.
* **Dataset Source:** Creditcard_data.csv.
* **Balancing:** The dataset was converted into a balanced class dataset using **SMOTE** (Synthetic Minority Over-sampling Technique) to ensure a 50/50 class distribution.

### 2. Sampling Strategies
Five unique sampling techniques were applied to create representative training subsets:
* **Sampling1 (Simple Random Sampling):** Randomly selecting instances from the population.
* **Sampling2 (Stratified Sampling):** Maintaining class proportions within the sample.
* **Sampling3 (Systematic Sampling):** Selecting every $k^{th}$ instance from the dataset.
* **Sampling4 (Cluster Sampling):** Dividing the data into clusters and selecting specific groups.
* **Sampling5 (Bootstrap Sampling):** Random sampling with replacement.

### 3. Machine Learning Models
The samples were evaluated across five different machine learning architectures:
* **M1:** Logistic Regression
* **M2:** Decision Tree
* **M3:** Random Forest
* **M4:** Support Vector Machine (SVM)
* **M5:** Gradient Boosting Classifier

---

## 📊 Result Analysis

The following table summarizes the accuracy (%) achieved by each combination of model and sampling technique based on our experimental results.

| Model \ Sampling | Simple Random | Stratified | Systematic | Cluster | Bootstrap |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Logistic Regression** | 91.94 | 91.94 | 95.16 | 90.32 | 95.16 |
| **Decision Tree** | 90.32 | 93.55 | 93.55 | 95.16 | 100.00 |
| **Random Forest** | 95.16 | 98.39 | 100.00 | 98.39 | 100.00 |
| **SVM** | 90.32 | 96.77 | 100.00 | 91.94 | 100.00 |
| **Gradient Boosting** | 93.55 | 96.77 | 95.16 | 96.77 | 100.00 |

---

## 📈 Key Findings
* **Winning Technique:** **Bootstrap Sampling** and **Systematic Sampling** consistently provided the highest accuracy across most models.
* **Winning Model:** **Random Forest** proved to be the most resilient model, achieving perfect or near-perfect accuracy with multiple sampling methods.
* **Conclusion:** Sampling techniques significantly influence model performance. Proper feature scaling and data balancing (SMOTE) are essential precursors to effective fraud detection modeling.

---

## 📂 Repository Structure
* `Creditcard_data.csv`: The processed dataset.
* `sampling.ipynb`: The Jupyter Notebook containing the full implementation.
* `sampling_results.csv`: Exported performance matrix.
* `README.md`: Project documentation.

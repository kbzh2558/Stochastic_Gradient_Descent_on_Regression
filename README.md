# 📈📊 Exploring the Effects of SGD on Linear and Logistic Regression
![Python](https://img.shields.io/badge/python-3.10%2B-blue?logo=python)
![Regression](https://img.shields.io/badge/Regression-linear_and_logistic-green)
![SGD](https://img.shields.io/badge/SGD-mini_batch-orange)

🔍 A Comprehensive Study on Regression Models and Optimization Strategies 🔍

> **Authors**  
> Mingshu Liu, Kaibo Zhang, and Alek Bedard  
> **Affiliation**: McGill University, COMP551 - Applied Machine Learning  
> **Date**: September 30, 2024  

---

## Overview

This project evaluates the performance of **Linear** and **Logistic Regression** models on two distinct datasets: the **Infrared Thermography Temperature Dataset** and the **CDC Diabetes Health Indicators Dataset**. It emphasizes the impact of preprocessing, mini-batch stochastic gradient descent (MB-SGD), and learning rate strategies on model efficiency and accuracy.

**Key Contributions:**
- Investigated the **effectiveness of MB-SGD** compared to analytical solutions.
- Explored the role of **preprocessing techniques**, including scaling and balancing.
- Evaluated **cross-validation** for consistent performance metrics.
- Analyzed **learning rate tuning** and its effect on model convergence.

---

## Dataset Description

### Infrared Thermography Temperature Dataset
- **Data Type**: Physiological data with temperature readings.
- **Size**: 1,008 rows and 34 columns (post-cleaning).  
- **Preprocessing Highlights**:
  - Addressed missing and invalid data values.
  - Balanced demographic imbalances to mitigate biases.
  - Removed categorical overlap in 'Age' feature.

### CDC Diabetes Health Indicators Dataset
- **Data Type**: Health behavior and condition data.
- **Size**: 253,680 rows and 22 columns.  
- **Preprocessing Highlights**:
  - Balanced classes (diabetic vs. non-diabetic) with a 1:3 ratio for improved model generalization.
  - Analyzed key variables like BMI and age for their influence on diabetes classification.

---

### Key Experiments

1. <details>
    <summary>Linear Regression Analysis</summary>

    - Evaluated R² and MSE on the Infrared dataset.
    - Achieved an R² of **0.7621** and test set MSE of **0.6698**, indicating a well-balanced fit.
   </details>

2. <details>
    <summary>Logistic Regression Evaluation</summary>

    - Assessed accuracy, precision, recall, and Log Loss on the CDC dataset.
    - Test set accuracy: **70.18%**; Precision: **29%**; Recall: **80%**.
   </details>

3. <details>
    <summary>Effect of Preprocessing</summary>

    - Balanced and scaled features to reduce variance and enhance convergence.
    - Improved training accuracy from **70.18%** to **78.40%** and testing accuracy to **83.52%**.
   </details>

4. <details>
    <summary>Cross-Validation</summary>

    - 5-fold CV showed improved stability:
      - Mean MSE for Linear Regression: **0.0708**.
      - Mean accuracy for Logistic Regression: **0.86** (post-preprocessing).
   </details>

5. <details>
    <summary>Mini-Batch SGD Optimization</summary>

    - Compared mini-batch sizes for convergence efficiency.
    - Linear regression achieved an MSE of **0.06** in **4.84 seconds** with batch size 16.
   </details>

6. <details>
    <summary>Learning Rate Tuning</summary>

    - Early stopping implemented for unstable learning rates.
    - Optimal learning rate **(α = 0.01)** reduced MSE to **0.63** for Linear Regression.
   </details>

7. <details>
    <summary>Analytical vs. MB-SGD Solutions</summary>

    - Analytical Linear Regression MSE: **0.0845**.
    - MB-SGD Linear Regression MSE: **0.0853**, demonstrating its scalability and efficiency.
   </details>

---

## Results Summary

| Model                        | Metric              | Value    |
|------------------------------|---------------------|----------|
| Linear Regression            | R² (Infrared)      | 0.7621   |
|                              | MSE (test)         | 0.6698   |
| Logistic Regression          | Accuracy (CDC)     | 70.18%   |
|                              | Precision          | 29%      |
|                              | Recall             | 80%      |
| Logistic Regression (preprocessed) | Accuracy (CDC) | 83.52%   |

---

## Insights and Future Work

- **Preprocessing** is critical for improving regression model reliability and convergence.  
- **Mini-batch SGD** effectively balances computational efficiency with accuracy.  
- **Learning rate tuning** significantly impacts convergence stability and model performance.  

Future explorations could include:
- Advanced feature engineering for more robust preprocessing.
- Experimenting with adaptive learning rates and optimization algorithms.
- Extending analyses to neural networks for nonlinear relationships.

---

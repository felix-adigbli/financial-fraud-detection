
# Financial Fraud Detection with Machine Learning

## **Overview**
This project explores the detection of fraudulent transactions in financial data using supervised and unsupervised machine learning techniques. The dataset's inherent imbalance and high stakes of fraud detection make this a challenging yet rewarding application of AI.

---

## **Objective**
The primary goals of the project are:
1. Minimize **false negatives** (undetected fraud) to prevent financial losses.
2. Reduce **false positives** (false alarms) to save operational costs.

---

## **Dataset**
- **Source**: Simulated credit card fraud detection dataset.
- **Size**: 284,807 transactions.
- **Fraud Prevalence**: Less than 0.2% of total transactions.
- **Features**: It contains only numerical input variables which are the result of a PCA transformation. 
     Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

---


## **Models Implemented**

### **Supervised Models**
1. Logistic Regression (Baseline)
2. Random Forest
3. XGBoost
4. LightGBM
5. Neural Networks

### **Unsupervised Models**
1. DBSCAN (Density-Based Spatial Clustering)
2. K-Means (Cluster-Based Anomaly Detection)
3. Autoencoders (Reconstruction-Based Anomaly Detection)

---

## **Evaluation Metrics**
Each model was evaluated using:
1. **Confusion Matrix Metrics**: TP, FP, TN, FN.
2. **Performance Metrics**: Accuracy, Precision, Recall, Specificity, F1 Score, ROC-AUC, PR-AUC.
3. **Cost-Sensitive Metrics**: False Negative Rate (FNR), False Positive Rate (FPR).
4. **Business Metrics**: Cost of Undetected Fraud, Cost of False Alarms.

---

## **Key Results**

### **Supervised Models**
| Model             | Accuracy | Precision | Recall | F1 Score | ROC-AUC | Cost of Fraud ($) | Cost of Alarms ($) |
|--------------------|----------|-----------|--------|----------|---------|-------------------|-------------------|
| Logistic Regression | 94.66%  | 97.59%    | 91.60% | 94.50%   | 98.87%  | 7,179,000         | 193,600          |
| Random Forest       | 99.99%  | 99.98%    | 100%   | 99.99%   | 99.99%  | 0                 | 1,700            |
| XGBoost             | 99.97%  | 99.94%    | 100%   | 99.96%   | 99.99%  | 0                 | 5,500            |
| LightGBM            | 99.90%  | 99.81%    | 99.99% | 99.90%   | 99.91%  | 3,000             | 16,100           |
| Neural Network      | 99.11%  | 98.36%    | 99.89% | 99.12%   | 99.95%  | 43,000            | 71,000           |

### **Unsupervised Models**
| Model         | Accuracy | Precision | Recall | F1 Score | ROC-AUC | Cost of Fraud ($) | Cost of Alarms ($) |
|---------------|----------|-----------|--------|----------|---------|-------------------|-------------------|
| DBSCAN        | 8.06%    | 1.22%     | 1.05%  | 1.13%    | 8.06%   | 281,328,000       | 24,146,000        |
| K-Means       | 51.94%   | 69.41%    | 6.94%  | 12.62%   | 59.96%  | 264,578,000       | 869,500           |
| Autoencoders  | 54.99%   | 99.98%    | 9.99%  | 18.18%   | 94.49%  | 76,766,000        | 200               |

---

## **Insights**
- **Supervised Models**: Random Forest and XGBoost delivered exceptional results, balancing recall, precision, and cost efficiency.
- **Unsupervised Models**: Autoencoders showed promise but require improvements in recall to be effective in fraud detection.
- **Business Costs**: Random Forest was the most cost-effective model, minimizing both undetected fraud and false alarms.

---

## **Next Steps**
- Refine unsupervised models to improve recall and precision.
- Incorporate hybrid models combining supervised and unsupervised techniques.
- Extend analysis with explainable AI (XAI) methods for better interpretability.




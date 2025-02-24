# Outlier Detection

### **Outlier Detection**

The **Outlier Detection** module identifies suspicious transactions that deviate significantly from normal behavior. This step helps in detecting fraudulent activities by flagging anomalies in customer transactions.

#### **Key Responsibilities**

1. **Global Outlier Detection**
   * Analyzes customer-level aggregated transaction behavior.
   * Flags unusual patterns across different customer clusters.
2. **Local Outlier Detection**
   * Focuses on individual flagged customers.
   * Analyzes specific transaction records for suspicious activities.
3. **Feature-Based Detection**
   * Uses transaction volume, frequency, and geographic risk indicators.
   * Applies multiple outlier detection algorithms for enhanced accuracy.

#### **Algorithms Used**

* **Isolation Forest**: Detects anomalies by isolating outliers in a tree structure.
* **Local Outlier Factor (LOF)**: Measures the density deviation of a data point from its neighbors.
* **One-Class SVM**: Identifies rare patterns by learning a boundary around normal data.
* **Autoencoders**: Deep learning model for unsupervised anomaly detection.
* **HBOS (Histogram-Based Outlier Score)**: Uses histogram density estimation to detect outliers.

#### **Modules Used**

* `model_utils.py`: Implements outlier detection models.
* `data_preparation.py`: Prepares transactional data for anomaly detection.

# Introduction (Overview, Scope, Architecture)

## Overview

The **Anti-Money Laundering (AML) System** is designed to detect and flag suspicious financial transactions. By leveraging a multi-step detection layers, the system identifies potentially fraudulent activities, helping financial institutions comply with AML regulations.

### Scope

The AML system focuses on **Two primary phases**:

1. **Unsupervised Phase.**

* _**Clustering and Segmentation:**_

Before detecting anomalies, the data undergoes an **unsupervised segmentation process**. This step involves grouping customers based on shared behaviors and transaction characteristics. By segmenting customers into clusters, the model can better understand the normal behavior of each group, which is crucial for identifying deviations that may indicate fraudulent activity. Clustering is a critical step because it ensures that the detection process is dynamic and sensitive to the inherent diversity in customer behavior. Customers exhibiting atypical behavior within their specific group are flagged for further investigation. This segmentation also helps reduce false positives by ensuring that comparisons are made between customers with similar profiles, making it easier to identify true outliers.



* **Global Outlier Detection**

This phase identifies anomalies in the output of the clustering algorithms, aiming to detect outliers in each cluster separately. The goal is to capture deviations that may indicate fraudulent behavior within specific customer clusters.



* **Local Outlier Detection**

After we have Flaged certain samples fromt he global phase which they where flaged as anomiles/outliers for that certain group they lies on, The Local Outlier detection start identifying suspicious transactions of that certain sample/customer and get his transactions, so we can now run another anomaly dectection algorithmis to detect fradualnt transaction in his transactions history. The core of this process involves detecting deviations in patterns such as transaction volume, frequency, and the geographic origin of funds. For instance, a sudden spike in transaction volume or frequency, or the involvement of high-risk countries, may be indicative of money laundering. These anomalies are flagged by the system for review by compliance teams. Rather than relying on a single model, our approach runs multiple outlier detection algorithms, each with unique parameters and adjustments, to ensure that no suspicious activity goes unnoticed. By using a hybrid methodology, the system maximizes its detection capabilities while minimizing false positives. Additionally, the flexibility of the solution allows it to adapt over time as new money laundering techniques evolve, keeping the detection process relevant and effective.

***





1. Supervised Phase



## Technology Stack

* **Programming Language**: Python
* **Database**: OracleDB
* **Libraries & Frameworks**:
  * **Data Processing**: `pandas`, `numpy`
  * **Machine Learning**: `scikit-learn`, `pyod`
  * **Logging & Monitoring**: `logging`
  * **Configuration Management**: `yaml`, `json`
  * **Database Handling**: `oracledb`

**Modules Used**

**Model Utilities**

* `pyod.models.knn`, `pyod.models.iforest`, `pyod.models.dif`, `pyod.models.lof`, `pyod.models.cblof`, `pyod.models.hbos`, `pyod.models.ecod`, `pyod.models.copod`, `pyod.models.abod`, `pyod.models.auto_encoder`, `pyod.models.deep_svdd`, `pyod.models.alad`, `pyod.models.feature_bagging`, `pyod.models.pca`, `pyod.models.kpca`
* **Clustering Algorithms**: `sklearn.cluster.KMeans`, `DBSCAN`, `AffinityPropagation`, `AgglomerativeClustering`, `SpectralClustering`, `Birch`
* **Gaussian Mixture Models**: `sklearn.mixture.GaussianMixture`
* **SHAP explanations for model interpretability**: `shap`

**Core System Components**

* **Main Execution**: `main.py`
* **Logging Utilities**: `logging_utils.py`
* **Configuration Handling**: `config_utils.py`
* **Data Utilities**: `data_utils.py`
* **Database Utilities**: `database_utils.py`
* **Data Preparation Utilities**: `data_preperation.py`
* **Description Utilities**: `description_utils.py`
* **Database Utilities**: `database_utils.py`










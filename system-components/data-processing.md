# Data Processing

#### **Data Processing**

The **Data Processing** module is responsible for handling raw transaction data, preparing it for analysis, and performing feature engineering. This step is crucial for ensuring that data is clean, structured, and suitable for model training and inference.

**Key Responsibilities**

1. **Data Ingestion**
   * Load transactional data from OracleDB.
   * Handle missing values and data inconsistencies.
   * Format data types appropriately.
2. **Feature Engineering**
   * Generate relevant features such as transaction frequency, amount variations, and risk indicators.
   * Perform normalization and scaling where necessary.
3. **Preprocessing Pipelines**
   * Apply transformations (e.g., log-scaling, one-hot encoding).
   * Store preprocessed data for model usage.

**Modules Used**

* `data_utils.py`: Handles query preparation and data retrieval.
* `data_preparation.py`: Performs feature engineering and preprocessing.

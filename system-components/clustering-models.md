# Clustering Models

### **Clustering Models**

The **Clustering Models** module is responsible for segmenting customers based on their transactional behavior. This segmentation helps in identifying unusual patterns and anomalies by comparing transactions within similar groups.

#### **Key Responsibilities**

1. **Customer Segmentation**
   * Group customers based on transactional similarities.
   * Use clustering techniques to define behavioral patterns.
2. **Feature-Based Clustering**
   * Utilize transaction frequency, amount, and risk indicators as clustering parameters.
   * Ensure dynamic clustering that adapts to evolving behaviors.
3. **Cluster Validation**
   * Evaluate cluster effectiveness using internal metrics (e.g., silhouette score).
   * Ensure that the clustering approach effectively separates different risk categories.

#### **Algorithms Used**

* **K-Means Clustering**: Groups customers based on distance metrics.
* **DBSCAN**: Identifies dense clusters and isolates outliers.
* **Affinity Propagation**: Finds optimal exemplars dynamically.
* **Agglomerative Clustering**: Merges clusters based on hierarchical relationships.
* **Gaussian Mixture Models**: Probabilistically assigns customers to clusters.
* **Birch Clustering**: Efficiently clusters large-scale data with incremental learning.

#### **Modules Used**

* `model_utils.py`: Implements clustering algorithms and initializes models.
* `data_preparation.py`: Prepares data for clustering.

## 1. Data Collection
- Dataset: StoresData.xlsx (150 stores, 25 variables).
- Key Variables: Sales $m, No. Staff, Location, Adv.$'000, HomeDel.

## 2. Data Preprocessing
- Fixed KeyError: Used "Adv.$'000".
- Encoded categorical variables (e.g., Location).
- Handled outliers: Capped extreme values (e.g., Sales $m).
- Applied log transformation to skewed data (e.g., No. Staff).
- Normalized features with StandardScaler.

## 3. Data Splitting
- Training: 120 samples, Testing: 30 samples.

## 4. Data Mining Techniques
# Hierarchical Clustering
- Used Ward's method and AgglomerativeClustering (3 clusters).
# Association Rule Mining
- Applied Apriori algorithm (min_support=0.1, min_confidence=0.5).

## 5. Evaluation Metrics
# - Hierarchical Clustering:
- Silhouette Score: ~0.45.
- Clusters: High-sales malls, low-sales strips, rural stores.
# - Association Rules:
- Key rules: {Location_1} → {HomeDel_1}, {Sales $m_High} → {No. Staff_High}.

## 6. Visualization
- Pie Chart: Cluster distribution (40%, 35%, 25%).
- Dendrogram: Showed hierarchical structure.
- Plots: Histogram (Sales $m), Scatter (Sales vs. Staff), Box (Sales by Location).

## 7. Conclusion
- Clusters: Identified 3 distinct store types.
- Rules: Staffing drives sales; malls offer delivery.
- Issues Fixed: KeyError, ModuleNotFoundError (mlxtend installed).
- Recommendations: Adjust staffing, advertising, and services by cluster.

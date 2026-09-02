# Targeted Marketing: E-Commerce Customer Segmentation via K-Means Clustering



> **Segments e-commerce customers using K-means, validated by the Elbow Method, Silhouette Scores, and heirarchal clustering to inform targeted marketing efforts to increase revenue.**



[![Current Project Status](https://img.shields.io/badge/Status-Actively_Refactoring-orange.svg)](#)



![Image of clusters derived in this work on PCA axes (left), with 20.7% and 44.3% explained variance, and t-SNE axes (right). A value of k = 5 was determined to be the optimal number of clusters from the Elbow Method, Silhouette Scores, and Heirarchal Clustering. Both dimensionality reduction techniques visually separate the identified clusters from one another. PCA shows distinct regions of single cluster type with some minor overlap at edges, whereas t-SNE separates clusters more clearly yet some data points fall away from the main cluster.](assets/pca_tsne_visualisation.png)



## ✦ Overview

- **Problem Statement:** The highly dimensional nature of e-commerce customer and order data brings difficulty in deriving actionable insights to effectively target customer groups.
- **Objective:** To engineer key customer features and apply clustering algorithms to segment the customer base into distinct profiles for comprehensive assessment and marketing reccomendations.
- **Impact:** By identifying distinct customer segments, businesses can tailor marketing strategies to improve retention, conversion, and overall customer lifetime value.



## ✦ Tech Stack

**Python**, **Pandas**, **NumPy**, **Scikit-learn (K-Means, PCA, t-SNE, StandardScaler)**, **SciPy**, **Matplotlib**, **Seaborn**



## ✦ Data

- **Source(s):** Multinational e-commerce dataset provided by SAS.
- **Size:** 951,669 records and 20 features before aggregation.
- **Notable Characteristics:** The dataset contains significant outliers representing high-value customers which must be preserved to capture critical customer demographics.



## ✦ Methodology

- **Preprocessing:** Features were engineered and aggregated by Customer ID before applying standardisation to give zero mean and unit variance for distance-based clustering methods.
- **Feature Engineering:** Engineered Frequency, Recency, Customer Lifetime Value (CLV), Age, and Average Unit Cost to collapse dimensionality whilst preserving strong customer profile characteristics.
- **Modelling:** K-Means selected for its efficiency in clustering large datasets, with the optimal k=5 derived using the Elbow method, Silhouette scores, and a hierarchal clustering dendrogram.
- **Evaluation:**  Evaluated cluster cohesion and separation via Silhouette Scores, ensuring the resulting customer segments were distinctly separated for effective interpretation, alongside the Elbow Method and a Ward Heirarchal Dendrogram for validation.



## ✦ Key Results and Outputs

- Identified 5 distinct customer profiles, including a high-frequency segment providing the highest CLV, and inactive customers suitable for proactive re-engagement efforts.
- Visualised cluster separation effectively using PCA and t-SNE dimensionality reduction techniques to confirm distinct segment boundaries.
- Delivered a comprehensive customer segmentation report outlining specific marketing strategies and business recommendations for each identified cluster.



## ✦ Roadmap and Limitations

- **Limitation:** t-SNE and hierarchal clustering are computationally expensive, requiring the use of data samples as opposed to the full dataset.
- **Future Work:**  Implement A/B testing via paired t-tests to statistically validate the impact of targeted marketing campaigns on the identified clusters.
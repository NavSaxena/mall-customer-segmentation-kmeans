# 🛍️ Customer Segmentation Using K-Means Clustering

An unsupervised machine learning project that segments retail mall customers into distinct groups based on their purchasing behavior using the K-Means clustering algorithm.

---

## 📋 Project Overview
Understanding customer behavior is essential for targeted marketing strategies. This project analyzes customer data to group individuals with similar spending habits and income levels, allowing businesses to tailor campaigns to specific segments (e.g., high-income high-spenders vs. budget-conscious shoppers).

---

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3.x
* **Data Manipulation & Analysis:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn (`KMeans`, `StandardScaler`)
* **Data Visualization:** Matplotlib

---

## 🔄 Project Workflow
1. **Data Loading & Inspection:** Loaded the Mall Customers dataset and performed exploratory data analysis (checking shape, missing values, and statistical summaries).
2. **Feature Selection:** Filtered key behavioral features—**Annual Income (k$)** and **Spending Score (1-100)**—to ensure clean 2D spatial clustering.
3. **Feature Scaling:** Applied `StandardScaler` to normalize features so income scale doesn't disproportionately dominate distance calculations.
4. **Elbow Method:** Evaluated inertia values across $K$ values from 1 to 10 to mathematically determine the optimal cluster count ($K=5$).
5. **Model Training & Prediction:** Trained the final K-Means model (`n_clusters=5`, `n_init=10`) and assigned cluster labels to each customer record.
6. **Visualization:** Generated an Elbow curve and a 2D scatter plot mapping customer groups alongside their respective cluster **Centroids** (inverse-transformed back to original dollar units).
7. **Export:** Saved the segmented dataset locally to `customer_segments.csv`.

---

## 📊 Key Results & Visualizations
* **Optimal Clusters ($K=5$):** Identified 5 distinct customer personas.
* **Centroid Mapping:** Visualized the center points of each cluster to clearly differentiate target demographics.

---

## 🚀 How to Run the Code
1. Clone this repository or download the files.
2. Ensure you have the required libraries installed:
   ```bash
   pip install pandas scikit-learn matplotlib

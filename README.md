# Bank Customer Segmentation (Unsupervised Learning)

## 📌 Project Overview
This repository contains a detailed Jupyter Notebook (`Bank Customer Segmentation (Unsupervised Learning).ipynb`) focused on customer segmentation for a banking dataset. The goal is to identify distinct groups of customers based on their financial profiles, demographics, and loan behaviors using unsupervised machine learning techniques like **K-Means Clustering** and **Hierarchical Clustering**.

By leveraging dimensionality reduction (**PCA**), the project aims to simplify the feature space while retaining the most significant variances in customer data, ultimately helping the bank tailor its marketing strategies for personal loans.

## 🛠️ Project Workflow
The analysis follows a rigorous unsupervised learning pipeline:

1.  **Exploratory Data Analysis (EDA) & Cleaning**:
    * Loading the bank dataset (`Bank_Personal_Loan.csv`).
    * Performing descriptive statistics to identify data distributions and potential anomalies.
    * **Feature Removal**: Dropping non-informative identifiers like `ID` and `ZIP Code`.
2.  **Advanced Pre-processing**:
    * **Multicollinearity Check**: Analyzing feature relationships using Spearman correlation and Variance Inflation Factor (VIF).
    * **Outlier Management**: Implementing an automated outlier capping mechanism using the **Interquartile Range (IQR)** method. 
    * **Standardization**: Applying `StandardScaler` to ensure all features contribute equally to distance-based clustering algorithms.
3.  **Dimensionality Reduction**:
    * Implementing **Principal Component Analysis (PCA)** to address multicollinearity and reduce computational complexity.
4.  **Clustering Implementation**:
    * **K-Means Clustering**: Determining the optimal number of clusters using the Elbow Method and Silhouette Scores.
    * **Hierarchical Clustering**: Generating Dendrograms using `scipy` and implementing Agglomerative Clustering to compare segment structures.
5.  **Cluster Evaluation & Interpretation**:
    * Analyzing the characteristics of the resulting segments (e.g., high-income clusters vs. low-usage clusters) to provide actionable business insights.

## ⚠️ Methodology & Computational Constraints
* **Task-Related Thresholds**: Please note that several parameters—such as the **0.7 correlation threshold** for multicollinearity and the specific **IQR capping logic** (applied only to columns with more than 2 unique values)—were determined according to the **specific requirements of this task**. While these might differ from standard general-purpose "best practices," they were optimized for the characteristics of this specific bank dataset.
* **Hardware Limitations**: Because the clustering algorithms and high-dimensional PCA transformations were carried out on a **local machine**, the model performances and the granularity of the search for optimal clusters (e.g., number of iterations) may be "not ideal." Limited computational resources restricted the ability to perform more exhaustive sensitivity analyses.

## 💻 Technologies Used
-   **Python 3.x**
-   **Data Analysis**: Pandas, NumPy
-   **Visualization**: Matplotlib, Seaborn
-   **Machine Learning**: Scikit-Learn (PCA, KMeans, AgglomerativeClustering)
-   **Statistical Analysis**: Statsmodels (VIF), Scipy (Hierarchy/Dendrograms)

## 🚀 How to Use
1.  **Dataset**: Ensure the file `Bank_Personal_Loan.csv` is located in the same directory as the notebook.
2.  **Dependencies**: Install the required libraries:
    ```bash
    pip install pandas numpy seaborn matplotlib scikit-learn statsmodels scipy
    ```
3.  **Execution**: Open `Bank Customer Segmentation (Unsupervised Learning).ipynb` and run the cells sequentially to observe the data transformation and the final customer segments.

---

*Created as part of a professional development exercise in Unsupervised Learning & Dimensionality Reduction.*

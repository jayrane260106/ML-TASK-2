# 🛍️ Customer Segmentation using K-Means Clustering

## 📌 Project Overview

This project is **Task 2 of my Machine Learning Internship**. The objective is to segment mall customers into meaningful groups using the **K-Means Clustering** algorithm.

The project uses the **Mall Customers dataset**, containing 200 customer records with information about Customer ID, Gender, Age, Annual Income, and Spending Score.

For clustering, the notebook selects **Annual Income (k$)** and **Spending Score (1-100)** as the main features.

## 🎯 Objectives

- Load and explore the Mall Customers dataset.
- Check dataset information, statistics, missing values, and duplicates.
- Analyze customer age, income, and spending-score distributions.
- Select relevant features for clustering.
- Standardize the selected features.
- Determine a suitable number of clusters using the Elbow Method.
- Compare cluster quality using Silhouette Scores.
- Apply K-Means clustering with **K = 5**.
- Visualize customer segments.
- Analyze the characteristics of each cluster.
- Create a final customer-segmentation profile.

## 📊 Dataset

**Dataset:** Mall Customers

**Records:** 200  
**Features:** 5

| Column | Description |
|---|---|
| CustomerID | Unique customer identifier |
| Gender | Customer gender |
| Age | Customer age |
| Annual Income (k$) | Annual income in thousands of dollars |
| Spending Score (1-100) | Customer spending score |

### Features Used for Clustering

- `Annual Income (k$)`
- `Spending Score (1-100)`

## 🤖 Algorithm: K-Means Clustering

K-Means is an unsupervised machine learning algorithm that divides data into a predefined number of clusters. Each customer is assigned to the cluster whose centroid is closest to the customer based on the selected features.

Before clustering, the features are standardized using `StandardScaler`.

## 📈 Model Selection

The notebook uses two methods to evaluate different values of K:

### Elbow Method

The inertia values are calculated for K values from 1 to 10. The resulting Elbow Curve helps identify a suitable number of clusters.

### Silhouette Score

The notebook calculates Silhouette Scores for K values from 2 to 10.

For the uploaded dataset and the notebook's settings, the highest calculated Silhouette Score is approximately **0.5547 at K = 5**.

Therefore, the project applies:

`K = 5`

## 📊 Cluster Analysis

Using K-Means with `K = 5`, the resulting cluster profile is:

| Cluster | Customers | Avg. Age | Avg. Income (k$) | Avg. Spending Score |
|---:|---:|---:|---:|---:|
| 0 | 81 | 42.72 | 55.30 | 49.52 |
| 1 | 39 | 32.69 | 86.54 | 82.13 |
| 2 | 22 | 25.27 | 25.73 | 79.36 |
| 3 | 35 | 41.11 | 88.20 | 17.11 |
| 4 | 23 | 45.22 | 26.30 | 20.91 |

These groups can be interpreted using income and spending behavior to understand different customer segments.

## 📉 Visualizations

The notebook contains visualizations for:

- Age distribution
- Annual income distribution
- Spending score distribution
- Customers before clustering
- Elbow Curve
- Silhouette Scores
- Customer clusters using K-Means
- Cluster centroids

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab / Jupyter Notebook

## 🔄 Project Workflow

```text
Load Dataset
     ↓
Explore & Clean Data
     ↓
Select Income & Spending Score
     ↓
Standardize Features
     ↓
Elbow Method
     ↓
Silhouette Score
     ↓
K-Means (K = 5)
     ↓
Assign Cluster Labels
     ↓
Visualize Clusters
     ↓
Analyze Customer Profiles
```

## 📁 Project Structure

```text
TASK 2 ML Internship/
├── TASK_2_ML_intership.ipynb
├── Mall_Customers.csv
├── Mall_Customers_Segmented.csv
└── README.md
```

## ▶️ How to Run

### Google Colab

1. Open `TASK_2_ML_intership.ipynb` in Google Colab.
2. Upload `Mall_Customers.csv` when prompted.
3. Run the notebook cells sequentially.
4. Review the clustering visualizations and cluster profile.

### Local Jupyter Notebook

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

Then open the notebook and run the cells sequentially.

## 🚀 Future Improvements

Future versions can include additional customer features, different clustering algorithms such as DBSCAN or hierarchical clustering, cluster validation, interactive visualizations, and customer-specific marketing recommendations.

## 👨‍💻 Author

**Jay Rane**

Machine Learning Internship – Task 2

## 📌 Conclusion

This project demonstrates how K-Means clustering can be used to segment customers based on annual income and spending behavior. The analysis provides a practical introduction to unsupervised machine learning and customer segmentation.

# Credit Card Customer Clustering

## Project Overview

This project aims to understand the different types of credit card customers by analyzing their spending habits and demographics. By grouping similar customers together, we can develop targeted marketing strategies that are more effective and efficient. The project analyzes data from 9,000 credit card users over the past six months and uses machine learning techniques to identify distinct customer segments. 

## Dataset

The dataset used in this project is from Kaggle and is publicly available: [CC GENERAL](https://www.kaggle.com/datasets/ccdata/data). It contains a wealth of information about credit card users, including:

* **Demographics:** Customer ID, tenure (how long they've been a customer)
* **Spending Habits:** Balance, purchases, cash advances, payments
* **Credit Behavior:** Credit limit, minimum payments, percentage of full payment 

This data is crucial for understanding customer behavior and identifying patterns.

## Methodology

The project follows a structured approach to ensure accurate and insightful results:

1. **Data Exploration and Descriptive Statistics:**  We start by examining the dataset to understand the basic characteristics of the data, such as the distribution of values, summary statistics (mean, median, etc.), and any missing data. This step helps us get familiar with the data and identify potential issues.
2. **Data Visualization (Exploratory Data Analysis):**  Using visualizations like histograms, scatter plots, and correlation matrices, we explore relationships between different variables in the dataset. This visual exploration helps us identify patterns and trends that might not be immediately obvious from the raw data. 
3. **Feature Engineering & Data Pre-processing:** To prepare the data for clustering, we handle missing values (using imputation techniques),
4. Before applying the clustering algorithm, we assess the clustering tendency of the data using the Hopkins statistic. This test helps determine if the data is suitable for clustering or if it's randomly distributed. scale features to ensure they have equal weight in the analysis, and apply dimensionality reduction (PCA) to simplify the data while preserving important information. This step is crucial for improving the performance and interpretability of the clustering model.
5. **Clustering Model:** We employ the K-Means clustering algorithm to group customers with similar characteristics into clusters. K-Means works by iteratively assigning data points to clusters based on their distance from cluster centers (centroids).
6. **Evaluate the Clustering Performance:** We use metrics like the Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index to assess the quality of the clusters. These metrics help us determine how well-separated the clusters are and how similar data points are within each cluster.
7. **Calculate Cluster Profiles:**  After identifying the clusters, we analyze the average values of each feature within each cluster to create a profile of the typical customer in that segment. This helps us understand the defining characteristics of each customer group.
8. **Marketing Strategy Suggestions:** Based on the insights gained from the cluster profiles, we formulate tailored marketing strategies for each customer segment. These strategies are designed to be more relevant and effective by addressing the specific needs and preferences of each customer group.


## Results

The K-Means clustering algorithm identified three distinct customer segments, as shown in the plot below:

![image](https://github.com/user-attachments/assets/86d1066b-cece-4483-8f8e-5040434eb7c1)


**Interpretation:**

- **Cluster 0 (Purple):** Represents the "Big Spenders / High-Value Customers" segment.
- **Cluster 1 (Green):** Represents the "Regular Users / Transactors" segment.
- **Cluster 2 (Yellow):** Represents the "Inactive Users / Revolvers" segment.

The plot visualizes the clusters based on the two principal components derived from the original features. The separation between the clusters suggests distinct customer behaviors and characteristics.

The clustering analysis reveals three distinct customer segments:

1. **Big Spenders / High-Value Customers:**  These customers tend to have high credit limits, maintain high balances, make frequent purchases, and consistently make high payments. They are likely to be long-term customers with a strong financial standing.
2. **Regular Users / Transactors:**  These customers exhibit moderate spending habits, consistent purchase patterns, and typically pay their bills in full. They are reliable users of their credit cards for everyday transactions.
3. **Inactive Users / Revolvers:** These customers have lower credit limits, infrequent purchases, and may rely more on cash advances. They tend to carry a balance and might be less engaged with their credit cards.


## Marketing Strategy Suggestions

Based on the identified customer segments, here are some potential marketing strategies:

- **Big Spenders:** Offer premium rewards programs, exclusive perks, personalized offers, and concierge services to enhance their experience and encourage further spending.
- **Regular Users:** Promote installment plans for larger purchases, partner with relevant merchants to offer targeted discounts, and encourage increased card usage through loyalty programs.
- **Inactive Users:**  Provide financial education resources, offer entry-level cards with lower credit limits to encourage responsible credit building, and consider upgrade paths to engage them more actively.


## Conclusion

This project highlights the power of customer segmentation in understanding and targeting different customer groups. By leveraging machine learning techniques, businesses can gain valuable insights into customer behavior and develop data-driven marketing strategies to improve customer engagement and drive business growth.


## Libraries Used

- pandas: For data manipulation and analysis
- numpy: For numerical computations
- seaborn: For statistical data visualization
- matplotlib: For creating static, interactive, and animated visualizations
- scikit-learn: For machine learning algorithms and tools
- opendatasets: For downloading datasets from online sources
- pyclustertend: For assessing cluster tendency in data


## References
- Kaggle notebook - clustering on Credit Card Dataset

- Kmeans clustering - Jovian_Tutorials(unsupervised ML Algo)

- Hopkins Test - Medium Blog

- Scikit-Learn - Selecting the number of clusters with elbow method and silhouette analysis on KMeans clustering




## How to Run

1. **Clone the Repository:** Use `git clone` to download a copy of the project to your local machine.
2. **Install Libraries:** Use `pip install -r requirements.txt` to install the necessary Python packages. (Create a `requirements.txt` file listing the libraries)
3. **Run the Notebook:** Open and execute the Jupyter Notebook `Credit_Card_Customer_Clustering.ipynb` in your preferred environment (e.g., Google Colab, Jupyter Notebook). characteristics of each customer segment.




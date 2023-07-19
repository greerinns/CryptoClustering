# CryptoClustering
Clustering Cryptocurrencies using K-means and Principal Component Analysis (PCA)

This project aimed to cluster cryptocurrencies based on their market data using the K-means clustering algorithm and optimize the clusters using Principal Component Analysis (PCA). The following steps were performed:

## Data Loading and Exploration:
The "crypto_market_data.csv" file was loaded into a DataFrame, and summary statistics were computed to gain initial insights into the data. Additionally, data plots were created to visualize the distribution of the data.

## Data Preprocessing:
The data was preprocessed by normalizing it using the StandardScaler() module from scikit-learn. A new DataFrame was created with the scaled data, with the "coin_id" index from the original DataFrame set as the index for the new DataFrame.

## Finding the Best Value for k Using the Original Scaled DataFrame:
The elbow method was applied to determine the optimal number of clusters (k) for the K-means algorithm. The inertia values were computed for different k values, and a line chart was plotted to visually identify the best k value.

## Clustering Cryptocurrencies with K-means Using the Original Scaled Data:
K-means clustering was performed on the original scaled data using the best k value obtained from the elbow method. The K-means model was fitted to the data, and the clusters were predicted. A scatter plot using hvPlot was created, with "PC1" and "PC2" as the x-axis and y-axis, respectively, and color-coded by the cluster labels. The "coin_id" column was included in the hover_cols parameter to identify each cryptocurrency in the plot.

## Optimizing Clusters with Principal Component Analysis (PCA):
PCA was performed on the original scaled data to reduce the features to three principal components. The explained variance was retrieved to assess how much information each principal component explained. The total explained variance of the three principal components was calculated and recorded in the notebook.

## Clustering Cryptocurrencies with K-means Using the PCA Data:
K-means clustering was performed on the PCA-reduced data using the best k value obtained from the elbow method. The K-means model was fitted to the data, and the clusters were predicted. A scatter plot using hvPlot was created, with "price_change_percentage_24h" and "price_change_percentage_7d" as the x-axis and y-axis, respectively, and color-coded by the cluster labels. The "coin_id" column was included in the hover_cols parameter to identify each cryptocurrency in the plot.

## Impact of Using Fewer Features for Clustering:
The project addressed the impact of using fewer features for clustering data using K-means. This impact was observed when clustering was performed on the original scaled data compared to the PCA-reduced data. The best value for k was recorded for both cases, and any differences were noted and analyzed.

## Conclusion
By following these steps, the project successfully clustered cryptocurrencies based on their market data and provided insights into the optimal number of clusters and the impact of using PCA for dimensionality reduction in the clustering process.






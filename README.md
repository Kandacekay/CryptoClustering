# CryptoClustering
## Project Overview
CryptoClustering is a Python-based project that leverages unsupervised learning techniques to predict whether cryptocurrencies are affected by 24-hour or 7-day price changes. The primary goal is to use the K-means clustering algorithm to group cryptocurrencies based on their price change patterns.

## Project Execution
### Data Preparation
1. Data Loading and Exploration:
   - The crypto_market_data.csv file is loaded into a DataFrame.
   -  Summary statistics are computed, and the data is plotted to gain insights into its structure.
2. Data Normalization:
   - The StandardScaler() module from scikit-learn is employed to normalize the data.
3. Scaled DataFrame Creation:
   - A new DataFrame containing the scaled data is created.
   -  The "coin_id" index from the original DataFrame is set as the index for the new DataFrame.

## Clustering with Original Scaled Data
1. Determining Optimal k:
   - The elbow method is implemented to find the best value for k.
   - A line chart visually depicts the inertia values for different k values, aiding in the identification of the optimal k.
2. K-means Clustering:
   - The K-means model is initialized with the optimal k value.
   - The model is fitted using the original scaled DataFrame.
   - Predicted clusters are assigned to group cryptocurrencies.
     
## Principal Component Analysis (PCA)
1. PCA and Feature Reduction:
   - A PCA model is created with n_components=3, reducing features to three principal components.
   - The explained variance is retrieved to understand the information attributed to each principal component.
2. PCA DataFrame Creation:
   - A new DataFrame with PCA data is generated, setting the "coin_id" index from the original DataFrame as the index.
     
## Clustering with PCA Data
1. Determining Optimal k with PCA:
   - The elbow method is applied to the PCA data to identify the best value for k.
2. K-means Clustering with PCA:
   - The K-means model is initialized with the optimal k value from PCA.
   - The model is fitted using the PCA data.
   - Predicted clusters are assigned to group cryptocurrencies.

## Deployment and Submission
1. GitHub Repository Management:
   - The project is submitted through a GitHub repository.
   - Appropriate commit messages are provided for each file.

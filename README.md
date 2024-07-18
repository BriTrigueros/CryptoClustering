# CryptoClustering
# Crypto Clustering Project

In this challenge, you’ll use your knowledge of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

## Before You Begin

1. Create a new repository for this project called CryptoClustering. Do not add this homework to an existing repository.
2. Clone the new repository to your computer.
3. Push your changes to GitHub.

## Files

Download the following files to help you get started:

- [Module 19 Challenge files](link_to_files)

## Instructions

1. Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.
2. Load the `crypto_market_data.csv` into a DataFrame.
3. Get the summary statistics and plot the data to see what the data looks like before proceeding.

## Prepare the Data

1. Use the `StandardScaler()` module from scikit-learn to normalize the data from the CSV file.
2. Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the Original Scaled DataFrame

1. Use the elbow method to find the best value for k:
   - Create a list with the number of k values from 1 to 11.
   - Create an empty list to store the inertia values.
   - Compute the inertia with each possible value of k.
   - Plot a line chart to visually identify the optimal value for k.
2. Answer: What is the best value for k?

## Cluster Cryptocurrencies with K-means Using the Original Scaled Data

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the original scaled DataFrame.
3. Predict the clusters to group the cryptocurrencies.
4. Create a scatter plot using hvPlot:
   - Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
   - Color the graph points with the labels found using K-means.
   - Add the "coin_id" column in the hover_cols parameter.

## Optimize Clusters with Principal Component Analysis (PCA)

1. Perform PCA on the original scaled DataFrame to reduce features to three principal components.
2. Retrieve the explained variance and answer: What is the total explained variance of the three principal components?
3. Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

## Find the Best Value for k Using the PCA Data

1. Use the elbow method on the PCA data to find the best value for k:
   - Create a list with the number of k values from 1 to 11.
   - Create an empty list to store the inertia values.
   - Compute the inertia with each possible value of k.
   - Plot a line chart to visually identify the optimal value for k.
2. Answer: What is the best value for k when using the PCA data? Does it differ from the best k value found using the original data?

## Cluster Cryptocurrencies with K-means Using the PCA Data

1. Initialize the K-means model with the best value for k.
2. Fit the K-means model using the PCA data.
3. Predict the clusters to group the cryptocurrencies using the PCA data.
4. Create a scatter plot using hvPlot:
   - Set the x-axis as "PC1" and the y-axis as "PC2".
   - Color the graph points with the labels found using K-means.
   - Add the "coin_id" column in the hover_cols parameter.

## Conclusion

Answer the following question:
- What is the impact of using fewer features to cluster the data using K-Means?

## Dependencies

- Python
- pandas
- NumPy
- scikit-learn
- hvPlot

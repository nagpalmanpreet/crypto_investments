# <span style="color:Navy">Module 10 Application</span>
##  <span style="color:Navy">Challenge: Crypto Clustering</span>
In this Challenge, you’ll combine your financial Python programming skills with the new unsupervised learning skills that you acquired in this module.

The CSV file provided for this challenge contains price change data of cryptocurrencies in different periods.

The steps for this challenge are broken out into the following sections:

*   Import the Data (provided in the starter code)
*   Prepare the Data (provided in the starter code)
*   Find the Best Value for k Using the Original Data
*   Cluster Cryptocurrencies with K-means Using the Original Data
*   Optimize Clusters with Principal Component Analysis
*   Find the Best Value for k Using the PCA Data
*   Cluster the Cryptocurrencies with K-means Using the PCA Data
*   Visualize and Compare the Results


## <span style="color:Navy">Find the Best Value for k by Using the Original Data 

In this section, you’ll use the elbow method to find the best value for k by using the original data. To do so, complete the following steps:

1. Code the elbow method algorithm to find the best value for k. Use a range from 1 to 11.

2. To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

3. Answer the following question: What’s the best value for k?

## <span style="color:Navy">Cluster the Cryptocurrencies with K-Means by Using the Original Data</span>

In this section, you’ll use the K-means algorithm along with the best value for k that you found by using the original data. Specifically, you’ll use them to cluster the cryptocurrencies according to the provided price changes of the cryptocurrencies. To do so, complete the following steps:

1.   Initialize the K-means model with four clusters by using the best value for k.

2. Fit the K-means model by using the original data.

3. Predict the clusters for grouping the cryptocurrencies by using the original data. Review the resulting array of cluster values.

4. Create a copy of the original data, and then add a new column of the predicted clusters.

5. Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Colour the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents.


## <span style="color:Navy">Optimize the Clusters with Principal Component Analysis</span>

In this section, you’ll perform PCA and reduce the features to three principal components. To do so, complete the following steps:

1.  Create a PCA model instance, and set n_components=3.

2.  Use the PCA model to reduce the features to three principal components. Then review the first five rows of the DataFrame.

3.  Get the explained variance to determine how much information can be attributed to each principal component.

4. Answer the following question: What’s the total explained variance of the three principal components?

5. Create a new DataFrame with the PCA data. Be sure to set the coin_id index from the original DataFrame as the index for the new DataFrame. Review the resulting DataFrame.

## <span style="color:Navy">Find the Best Value for k by Using the PCA Data</span>

In this section, you’ll use the elbow method to find the best value for k by using the PCA data. To do so, complete the following steps:

1.  Code the elbow method algorithm, and use the PCA data to find the best value for k. Use a range from 1 to 11.

2.  To visually identify the optimal value for k, plot a line chart of all the inertia values computed with the different values of k.

3. Answer the following questions: What’s the best value for k when using the PCA data? Does it differ from the best value for k that you found when using the original data?

## <span style="color:Navy">Cluster the Cryptocurrencies with K-means by Using the PCA Data</span>

In this section, you’ll use the PCA data, the K-means algorithm, and the best value for k that you found by using the PCA data. Specifically, you’ll use them to cluster the cryptocurrencies according to the principal components. To do so, complete the following steps:

1.  Initialize the K-means model with four clusters by using the best value for k.

2.  Fit the K-means model by using the PCA data.

3.  Predict the clusters for grouping the cryptocurrencies by using the PCA data. Review the resulting array of cluster values.

4.  Create a copy of the DataFrame with the PCA data, and then add a new column to store the predicted clusters.

5.  Using hvPlot, create a scatter plot by setting x="price_change_percentage_24h" and y="price_change_percentage_7d". Colour the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents.

## <span style="color:Navy">Visualize and Compare the Results</span>

In this section, you’ll visually analyse the cluster analysis results by observing the outcome both with and without the use of optimisation techniques. To do so, complete the following steps:

1.  Create a composite plot by using hvPlot and the plus sign (+) operator to compare the elbow curve that you created from the original data with the one that you created from the PCA data.

2.  Create a composite plot by using hvPlot and the plus (+) operator to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data.

3.  Answer the following question: Based on visually analysing the cluster analysis results, what’s the impact of using fewer features to cluster the data by using K-means?
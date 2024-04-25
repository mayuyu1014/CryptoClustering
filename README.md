# CryptoClustering

# Unsupervised Machine Learning to study Crypto Currency data

# Data Normalization

* The first step is to getting the Z-score of every numerical value in the database, which is also called scaler transform.
* The StandardScaler from scikit-learn library is used to create a scaler object and perform the data transform.
* After normalization, the scaled data is now stored as a new data frame.

# Find the best K value

* Elbow method is used to determine the best k value for the number of clusters.
* A loop is used to try k from 1 to 11, and collects its corresponding inertia 
* The inertia values are then drew as a elbow graph to look for the point of diminishing return.
* And 4 is determined as the best value for k.

# K-Means clustering

* K-Means model is initiated with 4 clusters to train the scaled data.
* The trained model will predict the clusters and generate labels for each datapoint.
* Using hvplot to generate the clustering graph, the x axis is 24h change and the y is 7 day change.
* However, the clusters are not clearly seperated, which shows that these two features are not enough to distinguish the clusters.

# Principal Component Analysis

* PCA is used to reduce the dimensions of the origin dataset, to better understands the data as a whole.
* Initialite the PCA model with 3 components, which cover 90% of the original data in total
* Repeat the elbow method and K-Means model training for the PCA data.
* Plot the PCA dataset using hvplot, the clusters are seperated much clearer.
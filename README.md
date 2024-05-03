# CryptoClustering
Python Module 19 challenge for the U of M Data Analytics and Visualization Bootcamp (Unsupervised Learning)


## Plot your data to see what's in your DataFrame

![ss1](https://github.com/schr0841/CryptoClustering/blob/main/images/ss1.png)


We can see that there are stock tickers on the x-axis, and price change percentage on the y-axis, for many different periods ranging from 1 day to 200 days. It seems that the percentage change for 1 year is much higher for some of the stocks than the other variables. 


## Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.

![ss2](https://github.com/schr0841/CryptoClustering/blob/main/images/ss2.png)

By standardizing our dataframe, we can make sure all values are roughly in the same units. We perform k-means on a number of clusters ranging from 1 to 10 and plot the resulting inertias in a line plot known as an elbow curve. By analyzing the elbow curve, we determine that k=4 represents the optimal number of clusters, because the inertia decreases significantly from k=3 and there isn't much of a difference at either k=5 or k=6.  


## Cluster Cryptocurrencies with K-means Using the Original Data

![ss3](https://github.com/schr0841/CryptoClustering/blob/main/images/ss3.png)


## Optimize Clusters with Principal Component Analysis

![ss4](https://github.com/schr0841/CryptoClustering/blob/main/images/ss4.png)


## Compare elbow plots for PCA vs non-pca data

![ss5](https://github.com/schr0841/CryptoClustering/blob/main/images/ss5.png)



## Compare clustering for PCA vs non-pca data

![ss6](https://github.com/schr0841/CryptoClustering/blob/main/images/ss6.png)

The number of clusters remains unchanged (k=4 for both) but doing PCA on the data first allowed there to be more meaningful clustering of the data. In the non-PCA data there is one data point representing cluster 3 that is close to data from cluster 0, rendering this clustering not useful. The PCA data has the same number of clusters and also two different clusters that represent one data point each, but these points are far away from the other clusters. Therefore PCA does a better job figuring out the underlying important variables in the data and reducing the number of variables based on that. In the non-pca clustering case, it may be that other variables are more meaningful for the clusters rather than the two (7d and 24h price change percentage) that were chosen.







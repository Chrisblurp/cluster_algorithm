
TASK 4
You are given a large dataset with n data points, 
each of which has m features. 
come up with an algorithm that can cluster this data into k groups in less than O(n^2) time? 
How would you handle the case where the number of clusters k is not known in advance?

Solution

They are different styles of algorithm that can cluster the data into k groups in less than O(n^2) time, but the one used in this model
is the K-MEANS ALGORITHM

The k-means algorithm works as follows:

I Randomly select k points from the data as the initial centroids.
I Assign each data point to the centroid that is closest to it.
I Recalculate the centroid of each cluster as the mean of the data points assigned to it.
I Repeat steps 2 and 3 until the centroids no longer change.
This algorithm has a time complexity of O(k * n * m), where k is the number of clusters, n is the number of data points, and m is the number of features. 
In practice, the algorithm often converges in a few iterations, making it very efficient.

To handle the case where the number of clusters k is not known in advance,
we can use the elbow method or silhouette analysis to determine the optimal number of clusters. 
The elbow method involves running the k-means algorithm for different values of k and plotting the within-cluster sum of squares (WCSS) as a function of k. 
The "elbow" in the plot indicates the point of diminishing returns, where increasing k no longer significantly reduces the WCSS. 
Silhouette analysis measures how similar a data point is to its own cluster compared to other clusters. 
The optimal number of clusters is the one that maximizes the average silhouette width across all data points.

Alternatively, we can use a hierarchical clustering algorithm, which does not require specifying the number of clusters in advance. 
Hierarchical clustering creates a tree-like structure of clusters by successively merging the most similar clusters. 
The tree can be cut at a desired level to obtain the desired number of clusters. 
The time complexity of hierarchical clustering is O(n^2), which can be slow for large datasets, but there are faster variants that can be used in practice.

in my instance i used the elbow method to determine the optimal number of clusters when the number of clusters is not known in advance.
The elbow method involves running the k-means algorithm for different values of k and calculating the sum of squared distances,
of data points to their nearest cluster centroid. 
This sum of squared distances is also known as the inertia or within-cluster sum of squares.

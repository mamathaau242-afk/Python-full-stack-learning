# Day 19

## Key Learings

### Unsupervised Learning
There are two main categories of unsupervised learning that are mentioned below:
1. Clustering
2. Dimensionality Reduction Techniques
3. Association Rule Learning

### 1. Clustering
Clustering is an unsupervised machine learning technique used to group similar data points together without using labelled data. It helps discover hidden patterns or natural groupings in datasets by placing similar data points into the same cluster.
Common techniques include:
- K-Means
- DBSCAN
- Mean-shift

### K-Means Clustering 
Groups similar data points into clusters without needing labeled data. It is used to uncover hidden patterns when the goal is to organize data based on similarity.
- Helps identify natural groupings in unlabeled datasets
- Works by grouping points based on distance to cluster centers
- Commonly used in customer segmentation, image compression and pattern discovery
- Useful when you need structure from raw, unorganized data

### The algorithm works as follows:  
1. Initialization: We begin by randomly selecting k cluster centroids.
2. Assignment Step: Each data point is assigned to the nearest centroid, forming clusters.
3. Update Step: After the assignment, we recalculate the centroid of each cluster by averaging the points within it.
4. Repeat: This process repeats until the centroids no longer change or the maximum number of iterations is reached.

### DBSCAN Clustering
DBSCAN is a density-based clustering algorithm that groups data points that are closely packed together and marks outliers as noise based on their density in the feature space. It identifies clusters as dense regions in the data space separated by areas of lower density. Unlike K-Means or hierarchical clustering which assumes clusters are compact and spherical, DBSCAN perform well in handling real-world data irregularities such as:
- Arbitrary-Shaped Clusters: Clusters can take any shape not just circular or convex.
- Noise and Outliers: It effectively identifies and handles noise points without assigning them to any cluster.

### Steps in the DBSCAN Algorithm
Identify Core Points: For each point in the dataset count the number of points within its eps neighborhood. If the count meets or exceeds MinPts mark the point as a core point.
- Form Clusters: For each core point that is not already assigned to a cluster create a new cluster. Recursively find all density-connected points i.e points within the eps radius of the core point and add them to the cluster.
- Density Connectivity: Two points a and b are density-connected if there exists a chain of points where each point is within the eps radius of the next and at least one point in the chain is a core point. This chaining process ensures that all points in a cluster are connected through a series of dense regions.
- Label Noise Points: After processing all points any point that does not belong to a cluster is labeled as noise.

### Hierarchical Clustering
Hierarchical Clustering is an unsupervised learning technique that groups data into a hierarchy of clusters based on similarity. It builds a tree‑like structure (dendrogram) that helps visualize relationships and decide the optimal number of clusters.
- Does not require pre‑selecting the number of clusters.
- Uses agglomerative or divisive approaches.
- Commonly applied in data exploration and pattern discovery.
- It is commonly used in pattern recognition, customer segmentation and image grouping.

### Dendrogram
A dendrogram is like a family tree for clusters. It shows how individual data points or groups of data merge together. The bottom shows each data point as its own group and as we move up, similar groups are combined.

### Types of Hierarchical Clustering
Now we understand the basics of hierarchical clustering. There are two main types of hierarchical clustering.
- Agglomerative Clustering
- Divisive clustering

### Hierarchical Agglomerative Clustering
It is also known as the bottom-up approach or hierarchical agglomerative clustering (HAC). Bottom-up algorithms treat each data as a singleton cluster at the outset and then successively agglomerate pairs of clusters until all clusters have been merged into a single cluster that contains all data. 

### Hierarchical Divisive clustering
Divisive clustering is also known as a top-down approach. Top-down clustering requires a method for splitting a cluster that contains the whole data and proceeds by splitting clusters recursively until individual data have been split into singleton clusters.

### Computing Distance Matrix
While merging two clusters we check the distance between two every pair of clusters and merge the pair with the least distance/most similarity. But the question is how is that distance determined. There are different ways of defining Inter Cluster distance/similarity. Some of them are:
- Min Distance: Find the minimum distance between any two points of the cluster.
- Max Distance: Find the maximum distance between any two points of the cluster.
- Group Average: Find the average distance between every two points of the clusters.
- Ward's Method: The similarity of two clusters is based on the increase in squared error when two clusters are merged.

### 2. Dimensionality Reduction Techniques
Dimensionality reduction is a technique used to reduce the number of features in a dataset while preserving important information. It transforms high-dimensional data into a lower-dimensional space for simpler representation.
- Reduces computation time by lowering the number of features
- Helps prevent overfitting by removing irrelevant data
- Improves data visualization and understanding

### Principal Component Analysis (PCA)
PCA (Principal Component Analysis) is a dimensionality reduction technique and helps us to reduce the number of features in a dataset while keeping the most important information. It changes complex datasets by transforming correlated features into a smaller set of uncorrelated components.It helps us to remove redundancy, improve computational efficiency and make data easier to visualize and analyze.

### How it works step by step
Step 1: Standardize the Data
Step 2: Calculate Covariance Matrix
Step 3: Find the Principal Components
Step 4: Pick the Top Directions & Transform Data

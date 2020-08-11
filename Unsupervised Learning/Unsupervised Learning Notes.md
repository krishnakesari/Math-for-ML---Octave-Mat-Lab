
Def: Algorithm finds clusters in data

1. Market segmentation
2. Social network analysis - organize data centers better or organizing resources
3. Organizing computing clusters
4. Astronomical data analysis - understand galaxy formation 

# K-means clustering

1. Cluster assignment
2. Randomly initialize K cluster centroid points
3. Compute means and move centroid
4. Run iterations

input:
k - number of clusters
Training set 

# K-means for non-separated clusters
1. Cluster based on categories 
Eg: based on height and weight of client, cluster shirts into small, medium and large


# Optimization Objective or distortion cost function / distortion k means algorithm
Minimizing J (...) with respect to c(1), c(2)... c(m) while holding mu1, mu2, ... muk fixed

c(i) = index of cluster
Mu k = cluster centroid k 
Mu c(i) = cluster centroid of cluster to which x(i) has been assigned

# Random Initialization 

should have K < m (Randomly pick K training examples, where m = number of training examples)

Local optima - solutions where k means is stuck in local optima and not effective
Solution:  
1. Initialize k means multiple times 
2. Pick clustering that gave lowest cost J 

# Choosing number of clusters
1. Elbow method: 
x -axis K (no. of clusters); y -axis Cost function J
Choose the value in elbow shape where the elbow is 

2. K means based on a metric for how well it performs for that later purpose
Eg: Choose K means based on different sizes of T Shirts (Small, Medium, Large, Extra large) in this case k = 4

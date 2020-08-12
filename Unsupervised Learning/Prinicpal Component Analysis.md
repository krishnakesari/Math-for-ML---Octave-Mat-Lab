
# PCA problem function
Finds lower dimensional surface to project data 
Goal of PCA is to find a vector u(i) onto which to project data so as to minimize the projection error

Steps:
1. Reduce n-dimensions to k-dimensions
2. find a vector u(1)....u(k) onto which to project data so as to minimize the projection error

PCA is not linear regression 

# PCA Algorithm
Training set
Preprocessing (feature scaling/mean normalization (mu j))

Implementation Steps:
Reduce data from n-dimensions to k-dimensions through 
1. compute "Covariance Matrix" (Sigma)
2. Compute "eigenvectors" of matrix sigma: 
    [u,s,v]  = svd(Sigma);   svd means "Singular Value Decomposition"
3. Compute "Ureduce"
    Ureduce = U(:, 1:k);
    z = Ureduce` * x ;   Inverse of Ureduce multiplied by x

# Application of PCA

## Reconstruction from compressed representation 
Xapprox = Ureduce * z 


# choosing number of principal components (k value for PCA)
Minimize average squared projection error
Total variation in the data

1. Choose k to be smallest value so 99% of variance is retained (Eg: 0.01 or 0.05 or 0.10)

General Steps:
1. start with k = 1
2. compute Ureduce
3. Check if PCA <= 0.01 ?
4. Repeat ....

Efficient implementation steps: (Recommended method)
1. [u, s, v] = svd(Sigma)
2. 1 - mean value of sii <= 0.01

# Advice for applying PCA
## Supervised learning speedup

Steps:
1. Extract Input: unlabeled dataset  (eg: 10000 features)
2. Apply PCA (result: approximately 1000 features)
3. New training set and feed to learning algorithm to perform predictions
Note: This mapping can be applied to cross validation and test sets

To prevent overfitting: (use regularization instead of PCA)
Use z(i) instead of x(i) to reduce the number of features  to k < n 
Logic: Fewer features are less likely to overfit

### where you should not use PCA
General ML system design: (Important)
1. Get training set ((x(1), y(1)),....,(x(m), y(m)))
2. Run PCA to reduce x(i) in dimensions to get z(i)
3. Train logistic regression {(z(1), y(1)),....,(z(m), y(m))}
4. Test on test set: Map x test to z test and Run h theata(z) on {(ztest(i), ytest(i)),....,(ztest(m), ytest(m))}

Note: Try running whatever with original/raw data x(i) only if that doesn't do what you want - then implement PCA and consider using z(i)
a. only if running algorithm is taking longer












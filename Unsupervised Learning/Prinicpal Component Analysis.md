
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







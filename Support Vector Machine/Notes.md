# Optimization Objective

## gives more cleaner and perform complex learning functions

Alternative view of logistic regression 
sigmoid function
if y = 1, we want h(theta) > 0 and theta(Inverse T) x >> 0

1. From logistic regression replace -log theta ht theta(x(i)) with cost1(theta transpose x (i))
2. Remove 1/m terms from equation - that won't change optimal value
3. Cost term + Regularization term (Logistic Regression Eg: A + lambda B;  SVM Eg: CA + B) where C is 1/lambda)

## SVM Hypothesis
predict 1 if Theta transpose x >= 0

# Large Margin Classifier Intuition
## SVM Decision Boundary
Whenever y(i) = 1: Theta Transpose x(i) >= 1 ;  p(i) * ||theta|| >= 1
whenever y(i) = 0: Theta Transpose x(i) <= -1 ;  p(i) * ||theta|| <= -1
### Linearly separable Boundary
1. will have less marginal distance. It gives SVM Robustness
2. When there are outliers (Regularization constant C is very large): SVM will change decision boundary to accommodate outlier (Solution: Ignore outliers, if possible)

# Math behind Large Margin Classifier
## Vector Inner product
u transpose v = ?
||u|| = length of the vector u (# to measure euclidean distance) = Square root of u1 square + u2 square
p = length of projection of vector v onto vector u 
u transpose v = p * ||u|| = u1 * v1 + u2 * v2

# Kernel I
## Non-linear decision boundary
Given x, compute new features depending on proximity to landmarks l(1), l(2), l(3)....
1. Gaussian Kernel (Similarity function) => k(x, l(1))
f1 = similarity (x, l(1))
f2 = similarity (x, l(2))

kernels and similarity:
If x ~ l(1): f1 ~ 1
If x is far from l(1): f1 ~ 0  

Contour Plot will have x1 and x2 on horizontal access and f1 on y-axis 

# Kernel II
Choosing landmarks
SVM with Kernels 
x(i) ==> f1(i) ........... fm(i) = sim(x(i), l(1)) ........... sim(x(i), l(m))

## How to choose SVM parameters
C (= 1/lambda) 
Large C : Lower bias, high variance (small lambda) - over fitting
Small C : Higher Bias, low variance (large Lambda) - under fitting

Sigma square: 
Large: High bias, lower variance  (Gaussian Kernel vary more smoothly)
Small: Lower bias, high variance (Gaussian Kernel vary abruptly)


# using an SVM in Practice

## use liblinear, libsvm packages to solve for parameters theta.
Need to specify:
choice of parameters C
Choice of Kernel (Similarity function)

1. No kernel ("Linear kernel") to predict "y = 1" if theta transpose x > = 0 
    Use when n is large and m is small

2. Gaussian kernel: The best kernel
Need to choose sigma square 
n is small and m is large
Note: Perform feature scaling before using Gaussian Kernel
||v||^2 = ||x-l||^2

3. Polynomial Kernel (off-the-shelf kernel)

4. Other kernels:
Note: 
i. Not all similarity functions make valid kernels
ii. Need to satisfy "Mercer's Theorem" to make sure SVM packages optimizations run correctly and do not diverge



## Multi-class classification 
 Use one-vs-all method 

## Logistic regression vs SVM
if n is large (relative to m) - use logistic regression or SVM without a kernel ("Linear Kernel") (n = 10000, m = 10 - 1000)
If n is small, m is intermediate - use SVM with Gaussian Kernel (n = 1- 1000, m = 10 - 10000)
If n is small, m is large - manually create features / use logistic regression or SVM without a kernel  (n = 1 - 1000, m = 50000 + )















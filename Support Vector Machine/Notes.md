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










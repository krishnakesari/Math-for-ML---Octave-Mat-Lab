
# Monitoring machines in data center
Note: Don't model p(x1), p(X2),....p(xn) etc separately.
model p(x) all in one go

parameters: mu and sigma values (Covariance matrix)
            Where sigma is variance matrix and mu is mean matrix


# Anomaly Detection:
Steps:
1. fit model p(x)by setting mu and sigma values
2. Given a new example x, compute p(x)
   a. if p(x) < epsilon (threshold) return anomaly
   b. if p(x) >= epsilon (threshold) return normal

Relationship of gaussian distribution to the original model:
- Original model corresponds to multi-variate gaussian where covariance matrix sigma should be a diagonal matrix

# Original model vs Multivariate Gaussian model:

Original model:
1. Manually create features to capture anomalies where x1, x2, ... xn take unusual combinations of values (eg: x3 = x1/x2 etc.)
2. Computationally cheaper and scales better to large n values
3. Work fine, even with small training set

Multivariate Gaussian model:
1. Automatically captures correlations between features
2. Computationally more expensive as you should count inverse of sigma 
3. Must have m > n or else sigma is non-invertible
4. May not be accurate if you have redundant features (Eg: x1 = x2 (duplicate values) or x4 = x3 + x5)






# Density estimation 
steps:
1. Build model for p(x) - Probability of x
2. Identify unusual users 
   p(x test) < threshold --> flag anomaly
   p(x test) >= threshold --> 

# Gaussian distribution or normal distribution 
if x is a distributed gaussian with mean mu, variance (sigma)^2
p(x; mu, (sigma)^2)

## Parameter estimation problem:
estimating mu and (sigma)^2

# Anomaly Detection Algorithm
training set: {x(1), ... x(m)}
p(x) = p(x1)....p(xn)
x1 ~ N(mu1, (sigma1)^2) where N is normal distribution 
p(x1;mu1, (sigma1)^2)..........p(xn;mun, (sigma n)^2)

Implementation steps:
1. choose features xi that you think give analogous examples
2. Fit parameters mu1..........mu n, (sigma 1)^2............(sigma n)^2
3. Given new example of x, compute Gaussian probability p(x);  anomaly if p(x) < Epsilon where epsilon is the threshold value

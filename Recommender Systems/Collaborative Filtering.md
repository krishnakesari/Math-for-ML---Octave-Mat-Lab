
# Problem motivation 
- Data set without values on features

1. users tell how much they like a movie (parameters)
2. Based on parameters theta(1)...theta(j), we can predict features

## Optimization algorithm
Given theta(1)... theta(nu), to learn feature vector x(i): 

min J(theta)

# Collaborative filtering algorithm:
1. Initialize x(1),.........x(nm), theta(1).......theta(nu) to small random values
2. Minimize J using gradient descent (or an advanced optimization algorithm)
3. For a user with parameters theta and movie with (learned) features x we can predict (theta)^T * x


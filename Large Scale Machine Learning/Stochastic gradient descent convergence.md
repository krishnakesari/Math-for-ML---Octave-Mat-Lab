
# making sure gradient descent is converging 
1. cost function should decrease with every iteration

Steps:
1. compute cost(theta, (x(i), y(i))) before updating theta using (x(i), y(i))
2. Every 1000 examples plot cost function averaged over last 1000 example processed by algorithm

## Checking for convergence
Plot cost function, averaged over the last 1000 examples

Note: 
1. If plot is diverging use smaller alpha value
2. Can slowly decrease learning rage (alpha) to converge theta; 
   alpha = const1 / (Iteration number + const2)


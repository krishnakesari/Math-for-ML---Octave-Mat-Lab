
# Finding other related products to recommend user:

1. Group all ratings into a matrix

Y = Ratings, X = movies list, Theta = stack transposed parameters

## Low rank matrix factorization
For each product i, we learn a feature vector x(i)
x1 = romance, x2 = action .... xn = comedy 

## How to find movies j related to movie i ?
Distance between x(i) and x(j) is small, they are more likely same 
||x(i) - y(j)||





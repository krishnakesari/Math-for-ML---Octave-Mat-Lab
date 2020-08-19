
# Predicting movie ratings
1. user ratings from 0 - 5 stars

nu = no. of users
nm = no. of movies
r(i,j) = 1 if user j has rated movie j
y(i,j) = rating given by user (0-5)

Learning algorithm fills values for missing values (which user not yet given a score)

# Content based recommendation
1. convert each movie into a feature vector x(1) = [1, 0.0.9, 0]'
2. For each user j, learn a parameter theta(j) E R^3 dimensions.  predict user j as rating movie i with (theta(j))T. x(i) stars

Problem function:
r(i,j) = 1 if user j has rated movie i (0 otherwise)
y(i,j) = rating by user j on movie i (if defined)

theta(j) = parameter vector for user j
x(i) = parameter vector for movie i
for user j. movie i, predict rating: (theta(j))T. x(i)

m(j) = no. of movies rated by user j

To learn theta(j): 
(Treat as regression problem, as we are trying to predict value)



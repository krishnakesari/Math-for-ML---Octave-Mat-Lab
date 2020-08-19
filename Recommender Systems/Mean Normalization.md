
# User who have not rated any movies

if n = 2 (# of features)
theta(5) is the parameter vector for user 5 with no ratings

Implementation Steps:
1. Group all ratings into a matrix
2. Calculate each movie average rating among all users
3. Subtract original rating and average rating
4. From step 3 learn theta(i), x(i) 
5. each rating will be (theta(i))^T + mu(i)





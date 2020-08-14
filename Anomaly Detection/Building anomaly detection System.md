
# Developing and evaluating anomaly detection system

1. Way to evaluate an algorithm - to check if we improved or worsened with a feature addition/deletion
2. Assume we have some labeled data, of anomalous and non-anomalous examples (y = 0 if normal, y = 1 if anomalous)

Example data : 10000 good engines and 20 flawed engines
Training set: x(1)...x(n) - assume normal examples/not anomalous - 6000 examples - measure p(x)
Cross validation set - 2000 examples (y = 0), 10 anomalous (y = 1)
Test set - 2000 examples (y = 0), 10 anomalous (y = 1)

## Algorithm evaluation: 
 Steps:
 1. Fit model p(x) on training set
 2. On cross validation/ test examples x, predict
    y = 1 if p(x) < epsilon (anomaly);  
    y = 0 if p(x) >= epsilon (normal)

-- Evaluation Metrics:
a. Cross Evaluation - true positive, false positive, false negative, true negative
b. Precision/Recall
c. F1-Score

Note: Can also use cross-validation set to choose parameters

# Anomaly detection vs supervised learning
Anomaly detection:
1. very small number of positive examples (y=1). (0-20 is common)
2. large number of negative examples (y=0) 
3. there are many types of anomalies
    a. positive examples are too few
    b. Can not account for all possible anomalies
Recommended:  use Gaussian anomaly detection 
4. Applications: Fraud detection, aircraft manufacture, machines in data center

Supervised Learning:
1. Large number of positive and negative examples
2. More data 
    a. Enough examples to get a sense of positive examples
    b. Future positive examples likely to be similar to ones in training set
3. Applications: Email spam classification, weather prediction, cancer classification 














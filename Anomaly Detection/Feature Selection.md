
# Feature selection 

## Non-gaussian features: p(xi, mu i, (sigma i)^2)
1. Replace x1 with log(x1); 
2. you may use some other transformation x2 with log(x2+1);  x3 with square root of x3, x4 with cube root of x4

## Error analysis for anomaly detection 
Ideal scenario - p(x) large for normal examples of x
                 p(x) small for anomalous examples of x

Most common problem:
p(x) is comparable (say, both large) for normal and anomalous examples

## Feature selection for anomaly detection
1. Choose features that might take on unusually large or small values in the event of an anomaly



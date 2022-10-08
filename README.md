# Banknote-Classification-Project

Stakeholder: Banks who will want to detect the authenticity of bills

Dataset: U.C. Irvine took images of 714 real and 657 fake bills, via wavelet transformed analysis 
Background information on wavelet transformed analysis: 
https://www.youtube.com/watch?v=JdVq8Tn1ds0&t=350s

Objective: Present a bill to different machine learning algorithms, and determine whether the bill is real or fake 

# Features in the Dataset: 
Variance: dispersion (spread) of the image data
Skewness: the lack of symmetry of image data
Kurtosis: the lengths of tails in the distribution (a measure of outliers) of the image data
Entropy: measure of heterogeneity in the image data

 # Models:
Logistic Regression 
Decision Tree 
Random Forest 

# Logistic Regression (Tuning with C-regularization)
Before tuning with C-regularization, the logistic regression predicted 10 bills as the wrong type, but after tuning, the algorithm predicted only 6 as the wrong type. The model shows entropy is not important and skewness is the most important.

Random Forest was the best model and only predicted 1 bill as the wrong type 

# Conclusion 
Variance, Skewness, and Kurtosis of the image data were the most important features when classifying fake vs real bills
The logistic regression analysis determined skewness was the most important feature, but random forest determined variance was the most important 
Random forest was the most accurate model for banknote classification , with an accuracy score of 99.49%

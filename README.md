# Banknote-Classification-Project

Stakeholder: Banks who will want to detect the authenticity of bills

Dataset: U.C. Irvine took images of 714 real and 657 fake bills, via wavelet transformed analysis 
https://archive.ics.uci.edu/ml/datasets/banknote+authentication#

![Fake vs Real Distributions](https://i.imgur.com/UJujjDt.png)

Background information on wavelet transformed analysis: 
https://www.youtube.com/watch?v=JdVq8Tn1ds0&t=350s

Objective: Present a bill to different machine learning algorithms, and determine whether the bill is real or fake 

# Features in the Dataset: 
Variance: dispersion (spread) of the image data
Skewness: the lack of symmetry of image data
Kurtosis: the lengths of tails in the distribution (a measure of outliers) of the image data
Entropy: measure of heterogeneity in the image data

# Project Workflow: 
1. Split the data 
2. Scaled the data (organized it) 
3. Fit the model to the training data (provided the model with data) 
4. Made a pipeline for each model, sometimes with cross validation too
5. Made a confusion matrix (TN/TP, FN/FP grid)
6. Evaluated the model on the testing data: acc, prec, f1, best score
7. Made a predictive finding: How well the model is able to predict the target (Shows you which features are the most important)
8. Hyperparameter tuning 
9. Final model
10. Made predictive recommendations: Situations where predictions made by your model would and wouldn't be useful to the bank using this model

 # Models:
Logistic Regression 

Decision Tree 

Random Forest 

# Logistic Regression (Tuning with C-regularization)
Before tuning with C-regularization, the logistic regression predicted 10 bills as the wrong type, but after tuning, the algorithm predicted only 6 as the wrong type. The model shows entropy is not important and skewness is the most important.

![Confusion Matrix Before Tuning](https://i.imgur.com/YMeT8by.png)

![Confusion Matrix After Tuning](https://i.imgur.com/hzxApBB.png)

![Logistic Regression Feature Weights](https://i.imgur.com/8p7R3Tw.png)

# Decision Tree

![Decision Tree](https://i.imgur.com/usZ9Kv3.png)

# Random Forest 
The best model  was random forest. It only predicted 1 bill as the wrong type 

![Random Forest Confusion Matrix](https://i.imgur.com/gjhZ433.png)

![Random Forest Feature Weights](https://i.imgur.com/d3A1NSo.png) 

![Overall Model Comparison](https://i.imgur.com/c9KPl4X.png)

# Conclusion 
Variance, Skewness, and Kurtosis of the image data were the most important features when classifying fake vs real bills
The logistic regression analysis determined skewness was the most important feature, but random forest determined variance was the most important 
Random forest was the most accurate model for banknote classification, with an accuracy score of 99.49%

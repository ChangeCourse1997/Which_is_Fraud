# Which_is_Fraud
### The original file is too big to upload but can be found here https://www.kaggle.com/mlg-ulb/creditcardfraud

Credit Fraud Prediction
With the dataset from kaggle, it shows the details of transactions that have taken place in the span of 2 days and also labels the ones that were fradulent. I will use several models to fit the data which ill explain more.

## Logistic Regression Model
Uses a logit function that outputs values between 0 and 1. If the prediction is above 50%, then the classification is 1, else the classification will be 0.

## Suppport Vector Machines
 This model classifies with a decision boundary. Each observation plotted in n-dimensional space where n is number of features. 3-d space, decision plane, if more than 3-d, is hyperplane. SVM uses kernel trick that measures similarity in a higher dimensional space to make them linearly separable without actually doing a transformation. Can be time consuming for large datasets, but good when dimensions more than number of samples. Only uses a subset of training points.
 
 ## K Nearest Neighbors
 Sees the K nearest neighobrs of a data set and counts the votes of classification of the neighbors. The data set prediction will be the class with the highest number of votes.
 
 ## Gradient Boosted Decision Trees
Boosting means combining a learning algorithm in series to achieve a strong learner from many sequentially connected weak learners. In case of GBDT, the weak learners are decision trees. Each tree attempts to minimize the error of the previous tree, not using bootstrapping. Loss function like MSE and log loss are used for regression and classification accordingly. The added decision tree fits the residuals from the current model.
Learning rate(alpha) and n_estimators are two critical hyperparameters for gradient boosting decision trees. Each new tree modifies the model and magnitude of modification is the learning rate. N_estimator is the number of trees used in the model. Powerful versions are XGBOOST, LightGBM, CatBoost.
More accurate than random forest, no pre-processing is needed, however requires careful tuning of hyperparameters. More trees do not negatively affect random forest, but causes GB to overfit.

XGBoost is a sequential tree that uses parallel processing to increase speed. It works by using gradient descent to minimize the loss function.

## Random Forest
Uses a bunch of decision trees that are formed with bootstrapping which is random sampling with replacement and several features might be used more than once. The model counts the votes of all the trees and classifies the prediction base on the highest number of votes among the trees.

Thanks for reading :)

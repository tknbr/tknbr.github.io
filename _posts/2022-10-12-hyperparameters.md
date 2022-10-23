---
layout: post
title: Hyperparameters
categories: [ModelData]
---

**Hyperparameters** are parameters whose values **control the learning process** and determine the values of model parameters that a learning algorithm ends up learning. As a machine learning engineer designing a model, you choose and set hyperparameter values that your learning algorithm will use before the training of the model even begins. The hyperparameters will be different for each type of algorithm. As a consequence, **one must understand how a certain algorithm will learn and the role to play of each hyperparameter**. The value of each hyperparameter depends on the problem itself. To find the best hyperparameter for our problem, we will use a **grid search combined with [cross-validation](/cross-validation)**. Grid search is a technique where we create a matrix with all the parameters and values for each parameter we want to test and all possible combinations. Then, using cross-validation each set of hyperparameters will be evaluated. This process may be time consuming as the matrix will grow exponentially for each value to test.


```python
# Import from sklearn GridSearch function
from sklearn.model_selection import GridSearchCV
from sklearn import svm
  
# defining parameter range fro SVM 
# (check different values for hyperparameters Gamma & C)
param_grid = {'C': [0.1, 1, 10, 100, 1000], 
              'gamma': [1, 0.1, 0.01, 0.001, 0.0001]} 

# define hyperparameter best configuration search with 
# cross val (k=5)
grid = GridSearchCV(svm.SVC(), param_grid, cv=5)
  
# fitting the model for grid search
grid.fit(X_train, y_train)

```


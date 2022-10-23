---
layout: post
title: Regression and Classification algorithms
categories: [ModelData]
---

It's common to be overwhelmed when starting to build your first models about which algorithm use. We will later define a methodology where, for a certain problem, **several algorithms** will be tested to check which one will fit our problem best. My humble recomendation would be to start simple and learn step by step, don't try to introduce to many algoirthms in your selection process without understanding how they work or the parameters you are trying to tune.

When working with regression problems I would encourage you to start with this three diferent algorithms:

* **Linear Regression** (linear). One of the first algorithms to learn. Very basic and probably not the best but easy to understand and to tune. 
* **Decision Trees** (non-linear). Not as straightforward as linear regression, but quite simple to understand as well. This is the base to later learn about random forests, adaboost, xgboost, lightgbm, etc. Make sure to understand how it works and the parameters to tune it. Decision trees and their predecesors will be usefull not only when working with regression but also with classification.
* **Support Vector Regressor** (linear). A little bit more complex than decision trees, a bit more of math to learn. Very interesting concept and, personally, it works quite well. **IMPORTANT** this algorithm comes from support vector machine (SVM) algorithm, a classification algorithm. Please, first try to understand SVM and later expand your knowledge with support vector regressor.

If you are working with a classification problem, you can start with this three:


* **Decision Trees**. Voilà, you already did some work with regression for this algorithm. Check and example of how it is used with classification but it should be straight forward to learn.
* **Support Vector Machine**. Again, if you already understand SVR, SVM is just a simple case!
* **K-Nearest Neighbour**. Is a pattern recognition algorithm and also one of the first to learn. 
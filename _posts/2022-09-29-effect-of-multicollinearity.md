---
layout: post
title: Effect of multicollinearity
categories: [EDA]
---

After [preparing the data for consumption](/a-data-science-framework/), it is important to determine whether variable multicollinearity is present among our features. The ultimate goal will be to use N independent variables (X) to predict a dependent variable (y). Therefore, correlation between independent variables must be avoided. Correlation is the mutual relationship, covariation or association between two or more variables. An example of variables with a correlation can be a company's monthly sale and a company's monthly revenues.

A key goal in regression analysis is to isolate each independent variable's relationship and the dependent variable. So change in one independent variable shouldn’t affect any other variables in the given data. As the severity of the multicollinearity increases, so do these problematic effects. So during the fitting of the model, a small change in one variable can lead to a significant amount of swing in the model output. However, these issues affect only those independent variables that are correlated.

As a summary, the key aspects are:

* The severity of the problems increases with the degree of multicollinearity. Therefore, if you have only moderate multicollinearity, you may not need to resolve it.

* Multicollinearity affects only the specific independent variables that are correlated.

* If one of the collinear features has not much to contribute much to prediction or classification for distance-based ml algorithms, we can drop the analysis feature.

To analyse feature correaltion we can use one of the following methods:

1. **[Pearson’s correlation of coefficient](/pearson/)**. Used to measure of the strength of a **linear** association between two variables.
2. **[Spearman’s correlation of coefficient](/spearman)**. Non-parametric measure of the strength and direction of association that exists between two variables.
3. **[Kendall’s Tau correlation of coefficient](/kendall)**. Non-parametric measure of relationships between columns of ranked data.
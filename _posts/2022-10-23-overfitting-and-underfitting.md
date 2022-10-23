---
layout: post
title: Overfitting & Underfitting
categories: [ModelData]
---

As it has previously seen, the goal in Machine Learning is to approximate a target function using training data and later check the performance against a testing set. Generalization refers to how well the concepts learned by a machine learning model apply to specific examples not seen by the model when it was learning. A good generalization allows us to make predictions in the future on data the model has never seen. But, what happens when generalization does not occur?

* **Underfitting**: refers to a model that can neither model the training data nor generalize to new data. A clear sign of underfitting is when it will have poor performance on the training data.

* **Overfitting**: refers to a model that models the training data too well. It happens when a model learns the detail and noise in the training data to the extent that it negatively impacts the performance of the model on new data. It is more likely to occur with nonparametric and nonlinear models that have more flexibility when learning a target function. As such, many nonparametric machine learning algorithms also include parameters or techniques to limit and constrain how much detail the model learns.
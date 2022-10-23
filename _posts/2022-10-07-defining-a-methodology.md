---
layout: post
title: Defining a methodology
categories: [ModelData]
---

After [preparing](/the-4-cs/) and [exploring](/effect-of-multicollinearity/) the data, the next step will be to build the model. The dataset has been divided into train and test in a previous step. It is crucial to define a clear methodology to select an algorithm, tune it and train the model. To keep it simple, let's define a simple but effective methodology.

1. **Define a [metric](/metrics)** or metrics for the evaluation.
2. **Select a set of [algorithms](/regression-and-classification-algorithms)** to be evaluated.
3. **Tune the [hyperparameters](/hyperparameters)** of all algorithms using cross-validation and the training dataset.
4. Use best hyperparameters of all algorithms to **train a model** using the whole training dataset.
5. **Final evaluation**.

![placeholder](/images/methodology.png){:style="display:block; margin-left:auto; margin-right:auto;"  width="75%"}
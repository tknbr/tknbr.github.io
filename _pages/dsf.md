---
layout: page
title: A data science framework
permalink: /a-data-science-framework/
---


I find it common for everybody, starting with data science problems, to skip all the basic steps and move forward to create new models immediately. To resolve this issue, I always encourage others to take this simple approach:

1. **Define the problem**. Problems before requirements, requirements before solutions, solutions before design and design before technology.

2. **Gather the data**. Don't try to reinvent the wheel, we live in an age where data is probably already collected somewhere. Locate your source and plan a strategy to gather it.

3. **Prepare data for consumption**. Once we have the data, we must process, extract and clean it before we can use it. 

    3.1. **[Importing libraries](/importing-libraries/)**  
    3.2. **[Meet & greet the data](/meet-and-greet-data/)**  
    3.3. **[The 4 Cs: Correct, complete, create and convert](/the-4-cs/)**  
    3.4. **[Dividing the data into train and test](/train-test)**  

4. **Explore the data (EDA)**. Use statistic methods to find potential problems, patterns, classifications, correlations and computations on the data.

    4.1. **[Effect of multicollinearity](/effect-of-multicollinearity/)**  
    4.2. **[Pearson’s correlation of coefficient](/pearson/)**  
    4.3. **[Spearman’s correlation of coefficient](/spearman/)**  
    4.4. **[Kendall’s correlation of coefficient](/kendall/)**

5. **Model and validate the data**. The set of data and expected outcomes will determine which algorithms to use. Choosing a bad model can lead, in the best case, to poor performance and, in the worst case, to a bad conclusion. Also, this step will be used to look for signs of overfitting, under fitting or generalization and to obtain the model's performance.

    5.1. **[Defining a methodology](/defining-a-methodology)**  
    5.2. **[Metrics](/metrics)**  
    5.3. **Cross-validation**  
    5.4. **[Hyperparameter tunning](/hyperparameters)**  
    5.5. **Regression algorithms**  
    5.6. **Classification algorithms**

6. **Optimize**. Iterate through the whole process to make it better and more robust.

![placeholder](/images/framework.png){:style="display:block; margin-left:auto; margin-right:auto;"  width="60%"}
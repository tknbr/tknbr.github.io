---
layout: post
title: Meet and greet the data
categories: [Python, PrepareData]
---

The first step after [importing the libraries](/importing-libraries/) will be to load the data. Panda's library can be used to load the data in our program from a CSV file with a single line of code:

```python
# Load data from a CSV file and store it in a variable
df = pd.read_csv('path/to.csv')
```

It is time to get general information on the dataset, columns and type of variables in each column. Panda's library provides several functions to obtain information about the dataset:

```python
# prints information about a DataFrame including the 
# index dtype and columns, non-null values and memory 
# usage
print(df.info())

# returns the first n rows for the object based on 
# position. It is useful for quickly testing if your
# object has the right type of data in it.
print(df.head())
```

Understanding the data from these two simple steps is essential. The number of rows will indicate the size of our dataset (the number of samples we could have) and the number/type of columns the features we have for each sample. 

Continue with [The 4 Cs: Correct, complete, create and convert](/the-4-cs//)
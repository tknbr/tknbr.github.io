---
layout: post
title: Meet and greet the data
categories: [Python, PrepareData]
---

The first step after [importing the libraries](/importing-libraries/) will be to load the data. CSV is a very common file format to store the data. Panda's library can be used to load the data in our program from a CSV file with a single line of code:

```python
# Load data from a CSV file and store it in a variable
df = pd.read_csv('path/to.csv')
```
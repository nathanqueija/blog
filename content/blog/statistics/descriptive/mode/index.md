---
title: Mode
date: "2021-06-13"
description: "Descriptive Statistics: Mode - what is the most common value?"
categories: ["Statistics", "Descriptive Statistics"]
---

In order to calculate the mode we need to know the number of ocurrences of a datapoint in a dataset.

`[9, 5, 8, 10, 7, 8]`

Imagine that this dataset represents the grades of all the students in a class of statistics. The grades can range from 0 to 10.

We want to know the numbers that occurs most frequent in the dataset.

| Number | Occurrences |
| ------ | ----------- |
| 9      | 1           |
| 5      | 1           |
| 7      | 1           |
| 8      | 2           |
| 10     | 1           |

The number 8 is the most frequent number in the dataset therefore it is the mode.

What is we had more than one value with the same number of occurrences in a data set?

`[9, 5, 8, 10, 7, 7, 8]`

| Number | Occurrences |
| ------ | ----------- |
| 9      | 1           |
| 5      | 1           |
| 7      | 2           |
| 8      | 2           |
| 10     | 1           |

We could either say that the dataset has no mode or that it is bi-modal, i.e., it has two modes: 7 and 8.

If there are more than 2 modes usually we say that the dataset has no mode because we want to have a clear mode that summarizes our dataset. Of course it depends on the purpose of each data analysis, but the purpose of the mode is to give a clear indicator of what is the most frequent value in a dataset.

## 🐍 Python

```python
from collections import Counter
dataset = [9,5,8,10,7,10]
frequencies = Counter(dataset)
print(frequencies)
print(f"The mode for the dataset is: {frequencies.most_common(1)[0][0]}")
```

    Counter({10: 2, 9: 1, 5: 1, 8: 1, 7: 1})
    The mode for the dataset is: 10

## 📚 Libraries

```python
from scipy.stats import mode
dataset = [9,5,8,10,7,10]
print(f"The mode for the dateset is: {mode(dataset).mode[0]}")
```

    The mode for the dateset is: 10

## 📒 Notebook

The link for the notebook can be found [here](https://github.com/nathanqueija/statistics/blob/master/1_descriptive_statistics/3_mode.ipynb)

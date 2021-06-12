---
title: Median
date: "2021-06-12"
slug: median
description: "Descriptive Statistics: Median - what is the center of my data?"
categories: ["Statistics", "Descriptive Statistics"]
---

Mean, similar to the mean, is also a measure of central tendency and it's purpose is to understand where is the center of the data.

In order to illustrate the concept of mean I'll use the following dataset:

`[9, 5, 8, 10, 7]`

Imagine that this dataset represents the grades of all the students in a class of statistics. The grades can range from 0 to 10.

To calculate the median we need:

1. Sort the dataset = `[5, 7, 8, 9, 10]`
2. We now have to find the number that is exactly in the middle: 8 is the median

But what if the dataset had an even number of datapoints? For example:

`[5, 7, 8, 9, 9, 10]`

What is the median in this case?

1. Find the two numbers in the middle, or split the dataset in the middle. The two numbers we're looking for will be the ones that are on the edges of each half

Half 1: `[5, 7, 8]` & Half 2: `[9, 9, 10]`

The two numbers we're looking for in this case are 8 an 9

2. Calculate the mean of the two numbers in the middle

(8 + 9) / 2 = 8.5 is the median

## 🐍 Python

```python
dataset_odd = [9,5,8,10,7]
dataset_odd.sort()
idx_element_middle = int(len(dataset_odd)/2)
element_middle = dataset_odd[idx_element_middle]
print(f"The median for this class is: {element_middle}")
```

    The median for this class is: 8

```python
dataset_even = [9,5,8,10,7,9]
dataset_even.sort()
idx_element_middle_left_half = int((len(dataset_even) / 2) - 1)
idx_element_middle_right_half = int(len(dataset_even) / 2)
mean_of_center_elements = (dataset_even[idx_element_middle_left_half] + dataset_even[idx_element_middle_right_half]) / 2
print(f"The median for this class is: {mean_of_center_elements}")
```

    The median for this class is: 8.5

We got the same results shown in the explanation section above. Now that we understand how to calculate the median we can use Numpy that will male our lifes much easier so we can focus on our work.

## 📚 Libraries

```python
import numpy as np
dataset_odd_np = [9,5,8,10,7]
dataset_even_np = [9,5,8,10,7,9]
print(f"The median for this class is: {np.median(dataset_odd_np)}")
print(f"The median for this class is: {np.median(dataset_even_np)}")
```

    The median for this class is: 8.0
    The median for this class is: 8.5

## 📒 Notebook

The link for the notebook can be found [here](https://github.com/nathanqueija/statistics/blob/master/1_descriptive_statistics/2_median.ipynb)

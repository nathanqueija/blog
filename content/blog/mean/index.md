---
title: Mean
date: "2021-06-12"
description: "Descriptive Statistics: Mean - what is the center of my data?"
---

# Mean

Mean is a measure fo central tendency. It's usually know as average, but in mathematical terms you'd recognize it as mean, also because there are different types of means that can be calculated. For the sake of simpliciclity I'll approach mean here with the same meaning as the average of a dataset.

In order to illustrate the concept of mean I'll use the following dataset:

[9, 5, 8, 10, 7]

Imagine that this dataset represents the grades of all the students in a class of statistics. The grades can range from 0 to 10.

How can we calculate the center of this data? What is the average grade of this class?

The mean is calculated by the sum of all observation divided by the number of observations.

#### Sample

$$ \bar{x} = \frac{1}{n}\left (\sum\_{i=1}^n{x_i}\right ) = \frac{x_1+x_2+\cdots +x_n}{n} $$

where:

- ${n}$ is the number os observations or size of the dataset
- $ \bar{x} $ is the mean of the dataset

#### Population

$$ \mu = \frac{1}{N}\left (\sum\_{i=1}^N{x_i}\right ) = \frac{x_1+x_2+\cdots +x_N}{N} $$

where:

- ${N}$ is the number os observations or size of the dataset
- $ \mu $ is the mean of the dataset

## 🐍 Python

```python
dataset = [9,5,8,10,7]
n = len(dataset)
mean = sum(dataset) / n
print(f"The mean or the average grade for this class is: {mean}")
```

    The mean or the average grade for this class is: 7.8

## 📚 Libraries

```python
import numpy as np
mean_np = np.mean(dataset)
print(f"The mean or the average grade for this class is: {mean_np}")
```

    The mean or the average grade for this class is: 7.8

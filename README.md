# PROGRAMMING-ASSIGNMENT-2

# INTENDED LEARNING OUTCOMES
 1. To identify the codes and functions incorporated in the Numpy library
 2. To be able to apply and use the different codes and functions in creating a Python program using a Numpy library

# README: Normalization and Divisible by 3 Problems

## Activities and Explanations

### 1. Normalization Problem

#### Objective:

Create a random 5×5 matrix and normalize its values using the formula:

```
Z = (X - mean) / std
```

#### How It Works:

* Generate a matrix using `np.random.rand(5, 5)`.
* Compute its mean and standard deviation.
* Apply normalization.
* Save result as `X_normalized.npy`.

#### Code:

```python
X = np.random.rand(5, 5)
X_normalized = (X - X.mean()) / X.std()
np.save('X_normalized.npy', X_normalized)
```

---

### 2. Divisible by 3 Problem

#### Objective:

Create a 10×10 matrix from the squares of the first 100 integers and find values divisible by 3.

#### How It Works:

* Generate values using `np.arange(1, 101) ** 2`.
* Reshape to 10×10.
* Extract divisible values using modulo operation.
* Save result as `div_by_3.npy`.

#### Code:

```python
squares = np.arange(1, 101) ** 2
A = squares.reshape(10, 10)
div_by_3 = A[A % 3 == 0]
np.save('div_by_3.npy', div_by_3)
```

---

## Summary

| Task           | Description                            |
| -------------- | -------------------------------------- |
| Normalization  | Standardized a 5×5 matrix              |
| Divisible by 3 | Filtered squared values divisible by 3 |
| Libraries Used | NumPy (`import numpy as np`)           |
| Output Files   | `X_normalized.npy`, `div_by_3.npy`     |


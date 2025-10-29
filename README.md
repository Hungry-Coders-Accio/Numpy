````markdown
#  NumPy - Quick Notes for Data Analysts

Welcome, analysts!   
This README is your **compact summary** of everything we covered in our NumPy lecture - a ready reference for revision and quick recall.  
You will also find a link to the **practice notebook** at the end to strengthen your hands-on skills.

---

##  1. Introduction to NumPy

- **NumPy** stands for *Numerical Python*.  
- It’s used for **fast mathematical operations**, **multi-dimensional arrays**, and **vectorized data processing**.  
- Key import:
  ```python
  import numpy as np
````

---

##  2. Array Creation

| Function                        | Description                     | Example                     |
| ------------------------------- | ------------------------------- | --------------------------- |
| `np.array()`                    | Create array from list or tuple | `np.array([1,2,3])`         |
| `np.zeros(n)`                   | Array of zeros                  | `np.zeros(5)`               |
| `np.ones(n)`                    | Array of ones                   | `np.ones((2,3))`            |
| `np.arange(start, stop, step)`  | Like Python `range()`           | `np.arange(0,10,2)`         |
| `np.linspace(start, stop, num)` | Evenly spaced numbers           | `np.linspace(0,1,5)`        |
| `np.random.randint(a,b,n)`      | Random integers                 | `np.random.randint(0,10,5)` |

---

##  3. Array Attributes

| Attribute | Meaning                  | Example              |
| --------- | ------------------------ | -------------------- |
| `.shape`  | Dimensions of array      | `(3,4)`              |
| `.ndim`   | Number of dimensions     | `2`                  |
| `.size`   | Total number of elements | `12`                 |
| `.dtype`  | Data type of elements    | `int32` or `float64` |

---

##  4. Indexing & Slicing

* Access elements: `arr[0]`, `arr[-1]`
* Slice range: `arr[1:5]`
* 2D indexing: `arr[row, col]`
* Example:

  ```python
  a = np.arange(1,13).reshape(3,4)
  a[1, 2]      # element at row 2, column 3
  a[:, 1:3]    # all rows, columns 2–3
  ```

---

##  5. Mathematical & Statistical Operations

| Operation         | Function                           | Example   |
| ----------------- | ---------------------------------- | --------- |
| Add / Subtract    | `+`, `-`                           | `arr + 5` |
| Multiply / Divide | `*`, `/`                           | `arr * 2` |
| Mean              | `np.mean(arr)`                     |           |
| Sum               | `np.sum(arr)`                      |           |
| Min / Max         | `np.min(arr)`, `np.max(arr)`       |           |
| Argmin / Argmax   | `np.argmin(arr)`, `np.argmax(arr)` |           |

---

##  6. Boolean Indexing & Conditions

* Masking:

  ```python
  arr[arr > 10]        # elements > 10
  arr[arr % 2 == 0]    # even numbers
  ```
* Replace values:

  ```python
  np.where(arr < 0, 0, arr)
  ```

---

##  7. Reshape, Stack, Split

| Operation | Function                 | Example                     |
| --------- | ------------------------ | --------------------------- |
| Reshape   | `arr.reshape(r,c)`       | `np.arange(6).reshape(2,3)` |
| Stack     | `np.hstack`, `np.vstack` | Combine arrays              |
| Split     | `np.split(arr, n)`       | Divide into parts           |

---

##  8. Random & Utility Functions

| Function             | Description         |
| -------------------- | ------------------- |
| `np.random.seed(42)` | Fix randomness      |
| `np.random.rand()`   | Random floats (0–1) |
| `np.unique(arr)`     | Unique elements     |
| `np.sort(arr)`       | Sort array          |

---

##  9. Broadcasting

* NumPy can perform operations on arrays of different shapes:

  ```python
  a = np.array([1,2,3])
  b = np.array([[10],[20],[30]])
  print(a + b)
  ```
* Adds every element of `a` to each row of `b`.

---

##  10. NumPy with Pandas

We often extract NumPy arrays from pandas DataFrames:

```python
import pandas as pd
df = pd.read_csv("students_scores.csv")
math = df["math"].values
np.mean(math)
```

Helps us perform vectorized math operations efficiently.

---

##  Practice Notebook

 **Practice all these concepts here:**
[NumPy_Practice_40Q.ipynb](https://drive.google.com/file/d/1ObvKOtv9NYv6M5hl3GlrTzzCLG82yQNJ/view?usp=drive_link)

Includes:

* 30 single-topic questions
* 5 mixed-concept problems
* 5 dataset-based questions using pandas + NumPy

---

##  Final Note

NumPy is the **heart of data analysis** — master it once, and everything from pandas to machine learning becomes easier.
Keep practicing small problems, experiment with reshaping and slicing, and soon you’ll start *thinking in arrays*.

> “If you can manipulate arrays, you can manipulate the world of data.” 

```
```

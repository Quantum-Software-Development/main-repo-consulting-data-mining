
# Variation Measures and Standard Deviation – Full Guide with Python Code

This guide explains key concepts about variation, deviation, variance, and standard deviation with step-by-step examples and formulas in LaTeX. Python code ready for Google Colab is included, cell-by-cell, with explanatory comments.

---

## 1. Variation

**Definition:**  
Difference between maximum and minimum values in a dataset.

\[ \text{Variation} = \text{Max value} - \text{Min value} \]

**Example:**  
Salaries (in thousands):  
41, 38, 39, 45, 47, 41, 44, 41, 37, 42

Ordered:  
37, 38, 39, 41, 41, 41, 42, 44, 45, 47  

Variation:  
\[ 47 - 37 = 10 \]

---

## 2. Deviation and Variance

### 2.1 Deviation of each value ($x$) from the mean ($\mu$):

Population deviation:  
\[ x - \mu \]

Sample deviation:  
\[ x - \bar{x} \]

### 2.2 Variance and Standard Deviation of Population

\[
\mu = \frac{\sum x}{N}
\]
\[
\sigma^2 = \frac{\sum (x - \mu)^2}{N}
\]
\[
\sigma = \sqrt{\sigma^2} = \sqrt{\frac{\sum (x - \mu)^2}{N}}
\]

---

## 3. Example – Population Variance & Standard Deviation

| Salary $(x)$ | $x - \mu$ | $(x - \mu)^2$ |
|-------------|-----------|---------------|
| 41          | -0.5      | 0.25          |
| 38          | -3.5      | 12.25         |
| 39          | -2.5      | 6.25          |
| 45          | 3.5       | 12.25         |
| 47          | 5.5       | 30.25         |
| 41          | -0.5      | 0.25          |
| 44          | 2.5       | 6.25          |
| 41          | -0.5      | 0.25          |
| 37          | -4.5      | 20.25         |
| 42          | 0.5       | 0.25          |
| **Sum**     |           | **88.5**      |

Variance:  
\[
\sigma^2 = \frac{88.5}{10} = 8.85
\]

Standard deviation:  
\[
\sigma = \sqrt{8.85} \approx 3.0
\]

---

## 4. Variance and Standard Deviation of Sample

\[
\bar{x} = \frac{\sum x}{n}
\]

\[
s^2 = \frac{\sum (x - \bar{x})^2}{n-1}
\]

\[
s = \sqrt{s^2}
\]

---

## 5. Python Code: Population and Sample Standard Deviation (Cell by Cell)

```


# Cell 1: Define data (salaries)

salaries =

```

```


# Cell 2: Calculate population mean

pop_mean = sum(salaries) / len(salaries)
pop_mean  \# Output expected: 41.5

```

```


# Cell 3: Calculate deviations squared for population

pop_sq_dev = [(x - pop_mean) ** 2 for x in salaries]
pop_sq_dev  \# Output: list of squared deviations

```

```


# Cell 4: Calculate population variance and std deviation

pop_variance = sum(pop_sq_dev) / len(salaries)
pop_std_dev = pop_variance ** 0.5
print(f"Population variance: {pop_variance}")
print(f"Population standard deviation: {pop_std_dev}")

```

```


# Cell 5: Calculate sample mean (same as population mean here)

sample_mean = pop_mean
sample_mean  \# Output: 41.5

```

```


# Cell 6: Calculate deviations squared for sample

sample_sq_dev = pop_sq_dev

```

```


# Cell 7: Calculate sample variance and std deviation

sample_variance = sum(sample_sq_dev) / (len(salaries) - 1)
sample_std_dev = sample_variance ** 0.5
print(f"Sample variance: {sample_variance}")
print(f"Sample standard deviation: {sample_std_dev}")

```

---

## 6. Grouped Data Standard Deviation Example

Suppose you have frequency data of children per household:

| Children $(x)$ | Frequency $(f)$ |
|----------------|-----------------|
| 0              | 10              |
| 1              | 19              |
| 2              | 7               |
| 3              | 7               |
| 4              | 2               |
| 5              | 1               |
| 6              | 4               |

Calculate mean and standard deviation with:

\[
\bar{x} = \frac{\sum (x \cdot f)}{N}
\]

\[
s = \sqrt{\frac{\sum f (x - \bar{x})^2}{N-1}}
\]

---

## 7. Python Code for Grouped Data (Cell by Cell)

```


# Cell 1: Define frequencies and values

x =[^1][^2][^3][^4][^5][^6]
f =[^1][^2][^4][^7][^10][^19]

```

```


# Cell 2: Calculate total frequency

N = sum(f)
N  \# Output expected: 50

```

```


# Cell 3: Calculate mean using weighted sum

mean = sum([xi * fi for xi, fi in zip(x, f)]) / N
mean  \# Output expected about: 1.82

```

```


# Cell 4: Calculate squared deviations (x - mean)^2

sq_dev = [(xi - mean) ** 2 for xi in x]
sq_dev  \# Output: list of squared deviations

```

```


# Cell 5: Calculate weighted squared deviations

weighted_sq_dev = [fi * sd for fi, sd in zip(f, sq_dev)]
weighted_sq_dev  \# Output: weighted squared deviations

```

```


# Cell 6: Calculate sample variance and std deviation

sample_variance = sum(weighted_sq_dev) / (N - 1)
sample_std_dev = sample_variance ** 0.5
print(f"Grouped data sample variance: {sample_variance}")
print(f"Grouped data sample standard deviation: {sample_std_dev}")

```

---

This completes the comprehensive guide on variation and standard deviation with formulas and stepwise Python code ready for running in Google Colab.



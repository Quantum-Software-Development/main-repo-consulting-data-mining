
# Variation Measures and Standard Deviation – Complete Guide

Based on the material: *Estatística Aplicada - Larson / Farber – Pearson (2010)*  
PUC-SP — Prof. Dr. Daniel Rodrigues da Silva

---

## 1. What is Variation?

**Variation** is the difference between the maximum and minimum entries in a quantitative data set.

\[
\text{Variation} = \text{Maximum Value} - \text{Minimum Value}
\]

- The data must be quantitative (numerical).

---

**Example: Calculating Variation**

A company hired 10 graduates. Their starting salaries (in thousand dollars):

```

41, 38, 39, 45, 47, 41, 44, 41, 37, 42

```

Ordered data:

```

37, 38, 39, 41, 41, 41, 42, 44, 45, 47

```

- Minimum: 37  
- Maximum: 47

\[
\text{Variation} = 47 - 37 = 10
\]

---

## 2. Deviation, Variance, and Standard Deviation

### 2.1. Deviation

**Deviation** for a value $x$ from the data set is:

- Population: $x - \mu$
- Sample: $x - \bar{x}$

---

### 2.2. Variance and Standard Deviation – Population

**Formulas:**

\[
\mu = \frac{\sum x}{N}
\]
\[
\sigma^2 = \frac{\sum (x - \mu)^2}{N}
\]
\[
\sigma = \sqrt{\frac{\sum (x - \mu)^2}{N}}
\]

where:
- $\mu$ is the population mean
- $N$ is the population size
- $\sigma^2$ is the variance
- $\sigma$ is the standard deviation

---

### Population Example

Salaries: `41, 38, 39, 45, 47, 41, 44, 41, 37, 42`  
Sum: $415$  
$\mu = 415 / 10 = 41.5$

| Salary ($x$) | $x - \mu$ | $(x - \mu)^2$ |
|--------------|-----------|--------------|
| 41           | -0.5      | 0.25         |
| 38           | -3.5      | 12.25        |
| 39           | -2.5      | 6.25         |
| 45           | 3.5       | 12.25        |
| 47           | 5.5       | 30.25        |
| 41           | -0.5      | 0.25         |
| 44           | 2.5       | 6.25         |
| 41           | -0.5      | 0.25         |
| 37           | -4.5      | 20.25        |
| 42           | 0.5       | 0.25         |
| **Total**    |           | **88.5**     |

\[
\sigma^2 = \frac{88.5}{10} = 8.85
\]
\[
\sigma = \sqrt{8.85} \approx 3.0
\]

> The population standard deviation is about $3.0$ (\$3,000).

---

### 2.3. Variance and Standard Deviation – Sample

**Formulas:**

\[
\bar{x} = \frac{\sum x}{n}
\]
\[
s^2 = \frac{\sum (x - \bar{x})^2}{n - 1}
\]
\[
s = \sqrt{s^2}
\]

where:
- $\bar{x}$ is the sample mean
- $n$ is the sample size
- $s^2$ is the sample variance
- $s$ is the sample standard deviation

---

#### Step-by-step Table (Sample Standard Deviation)

| Salary ($x$) | $x - \bar{x}$ | $(x - \bar{x})^2$ |
|--------------|---------------|-------------------|
| 41           | -0.5          | 0.25              |
| 38           | -3.5          | 12.25             |
| 39           | -2.5          | 6.25              |
| 45           | 3.5           | 12.25             |
| 47           | 5.5           | 30.25             |
| 41           | -0.5          | 0.25              |
| 44           | 2.5           | 6.25              |
| 41           | -0.5          | 0.25              |
| 37           | -4.5          | 20.25             |
| 42           | 0.5           | 0.25              |
| **Total**    |               | **88.5**          |

\[
s^2 = \frac{88.5}{10-1} = \frac{88.5}{9} = 9.83
\]
\[
s = \sqrt{9.83} \approx 3.1
\]

> The sample standard deviation is about $3.1$ (\$3,100).

---

## 3. Standard Deviation for Grouped Data (Frequency Distribution)

Formula for sample standard deviation from a frequency distribution (using midpoints $x$):

\[
s = \sqrt{\frac{\sum (x - \bar{x})^2 f}{n - 1}}
\]
where $f$ is the frequency for each class, $n = \sum f$

### Example

Number of children in 50 households (frequency table):

| $x$ (children) | $f$ | $x \cdot f$ |
|----|----|-----|
| 0  | 10 | 0   |
| 1  | 19 | 19  |
| 2  | 7  | 14  |
| 3  | 7  | 21  |
| 4  | 2  | 8   |
| 5  | 1  | 5   |
| 6  | 4  | 24  |
|**Total:**| **50** | **91** |

Sample mean:

\[
\bar{x} = \frac{91}{50} = 1.82
\]

Now, calculate squared deviations for each group and sum:

| $x$ | $f$ | $x - \bar{x}$ | $(x - \bar{x})^2$ | $(x - \bar{x})^2 \cdot f$ |
|---|---|-----------|--------------------|------------------|
| 0 | 10 | -1.82    | 3.31              | 33.10            |
| 1 | 19 | -0.82    | 0.67              | 12.73            |
| 2 | 7  | 0.18     | 0.03              | 0.21             |
| 3 | 7  | 1.18     | 1.39              | 9.73             |
| 4 | 2  | 2.18     | 4.75              | 9.50             |
| 5 | 1  | 3.18     | 10.11             |10.11             |
| 6 | 4  | 4.18     | 17.47             |69.88             |
| **Total** |  |  |  | **145.26**        |

Compute sample standard deviation:

\[
s = \sqrt{\frac{145.26}{49}} \approx \sqrt{2.965} \approx 1.72
\]

---

## 4. Quartiles, Interquartile Range and Boxplot

- **Quartile $Q_1$:** 25% of data below
- **Quartile $Q_2$:** (median) 50% of data below
- **Quartile $Q_3$:** 75% of data below

Interquartile Range (IQR):

\[
\text{IQR} = Q_3 - Q_1
\]

### Example

Test scores (ordered):

```

5, 7, 9, 10, 11, 13, 14, 15, 16, 17, 18, 18, 20, 21, 37

```

- $Q_1 = 10$
- $Q_2 = 15$
- $Q_3 = 18$

\[
\text{IQR} = 18 - 10 = 8
\]

---

## 5. Calculating Quartiles and Boxplots in Python

**Code Example:**

```

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_csv('banco.csv')

# Quartiles for the 'age' column

q1 = np.quantile(df['age'], 0.25)
q2 = np.quantile(df['age'], 0.5)
q3 = np.quantile(df['age'], 0.75)
print(f'Q1 = {q1}, Q2 (median) = {q2}, Q3 = {q3}')

# Boxplot

plt.boxplot(df['age'])
plt.title("Boxplot of Age")
plt.show()

```

---

## 6. Percentiles and Standard Scores (z-scores)

- **Percentiles ($P_k$):** Divide data into 100 equal parts
- **z-score:** Tells how many standard deviations a value is from the mean

\[
z = \frac{x - \mu}{\sigma}
\]

### Example

Forest Whitaker, age 45, won Best Actor. Average: 43.7, SD: 8.8  
Helen Mirren, age 61, won Best Actress. Average: 36, SD: 11.5

- Forest: $z = \frac{45 - 43.7}{8.8} \approx 0.15$
- Helen: $z = \frac{61 - 36}{11.5} \approx 2.17$

---

## 7. Summary Tables

### Types of Fractiles

| Fractile   | What it Divides             | Symbols       |
|:-----------|:---------------------------|:--------------|
| Quartiles  | Into 4 equal parts          | $Q_1, Q_2, Q_3$ |
| Deciles    | Into 10 equal parts         | $D_1, D_2, ..., D_9$ |
| Percentiles| Into 100 equal parts        | $P_1, P_2, ..., P_{99}$ |

---

## 8. Key Takeaways

- **Variation** and **standard deviation** measure the spread or scatter of data
- **Variance** uses squared deviations; **standard deviation** is the square root of variance
- **Sample** formulas use $n-1$ in denominator for unbiased estimation
- **Grouped data:** Use midpoints for classes; frequency-weighted calculations
- **Interquartile range (IQR)** is a robust measure of spread
- **Boxplot** visually displays data spread, median, quartiles, and outliers
- **z-scores** allow comparison between different data sets by standardizing values

---

You can use Python, Excel, or calculators to automate these calculations. For practical exercises and code, refer to the examples above.



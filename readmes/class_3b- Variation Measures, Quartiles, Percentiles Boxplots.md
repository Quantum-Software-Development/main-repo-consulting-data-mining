
# Variation Measures, Quartiles, Percentiles, and Boxplots – Full Guide with Python Code

This guide covers statistical concepts including variation, deviation, variance, standard deviation, quartiles, percentiles, and boxplots. It includes formulas in LaTeX, detailed explanations, and step-by-step Python code ready for execution cell-by-cell in Google Colab.

---

## 1. Variation and Standard Deviation

(Previously covered in detail; see above.)

---

## 2. Quartiles and Interquartile Range (IQR)

### Definitions:

- **Quartiles** divide an ordered data set into four approximately equal parts.
  
  | Quartile    | Description                        |
  |-------------|----------------------------------|
  | $Q_1$       | First quartile (25% data below)  |
  | $Q_2$       | Second quartile (Median) (50%)   |
  | $Q_3$       | Third quartile (75%)              |

- **Interquartile Range (IQR):**  
\[
\text{IQR} = Q_3 - Q_1
\]

### Example:

Data:  
`5, 7, 9, 10, 11, 13, 14, 15, 16, 17, 18, 18, 20, 21, 37`

- $Q_1 = 10$
- $Q_2 = 15$
- $Q_3 = 18$
- IQR = $18 - 10 = 8$

---

## 3. Percentiles

- Divide data into 100 equal parts.
- Example: The 72nd percentile means 72% of data fall below this value.

---

## 4. Boxplot

A graphical display showing:

- Minimum
- First quartile ($Q_1$)
- Median ($Q_2$)
- Third quartile ($Q_3$)
- Maximum

Useful for identifying spread, center, and potential outliers.

---

## 5. Python Code: Quartiles, Percentiles, and Boxplot (Step by step for Colab)

```


# Cell 1: Import necessary packages

import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

```

```


# Cell 2: Create sample data (can replace with actual data)

data =[^5][^7][^9][^10][^11][^13][^14][^15][^16][^17][^18][^20]

```

```


# Cell 3: Calculate quartiles

Q1 = np.percentile(data, 25)
Q2 = np.percentile(data, 50)  \# Median
Q3 = np.percentile(data, 75)

print(f"Q1 (25th percentile): {Q1}")
print(f"Q2 (Median, 50th percentile): {Q2}")
print(f"Q3 (75th percentile): {Q3}")

```

```


# Cell 4: Calculate Interquartile Range (IQR)

IQR = Q3 - Q1
print(f"Interquartile Range (IQR): {IQR}")

```

```


# Cell 5: Calculate specific percentile (e.g. 72nd percentile)

p72 = np.percentile(data, 72)
print(f"72nd percentile: {p72}")

```

```


# Cell 6: Generate boxplot

plt.boxplot(data)
plt.title("Boxplot of Sample Data")
plt.ylabel("Values")
plt.show()

```

---

## 6. Optional: Loading Numeric Columns from a CSV File for Quartile Analysis and Boxplots

```


# Cell 1: Import packages and load CSV file

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

df = pd.read_csv('your_file.csv')  \# Replace 'your_file.csv' with your filename

```

```


# Cell 2: View numeric columns

numeric_cols = df.select_dtypes(include=np.number).columns
print("Numeric columns in dataset:", numeric_cols)

```

```


# Cell 3: Calculate quartiles for a numeric column, e.g. 'age'

col = 'age'  \# Replace with your column name
Q1 = np.percentile(df[col], 25)
Q2 = np.percentile(df[col], 50)
Q3 = np.percentile(df[col], 75)

print(f"{col} Q1: {Q1}, Q2 (Median): {Q2}, Q3: {Q3}")

```

```


# Cell 4: Plot boxplot for the column

plt.boxplot(df[col])
plt.title(f"Boxplot of {col}")
plt.ylabel(col)
plt.show()

```


# Introduction to Data Mining with Python - Class 1

##  Overview

This repository contains materials and examples for the **Introduction to Data Mining with Python Class 1** course, focusing on fundamental statistical concepts and data analysis techniques essential for data mining applications.

## Class_1 Content

### Syllabus (Ementa)

- **Descriptive Statistics Review**
- **Data Mining Concepts**
- **Exploratory Data Analysis**
- **Predictive Analysis**
- **Clustering**
- **Association Rules**

### Assessment Criteria

- Minimum 75% attendance required
- Final grade ≥ 5.0
- Formula: MF = (N₁ + N₂)/2, where Nᵢ = (Pᵢ + Aᵢ)/2
  - Pᵢ = Project grade for semester i
  - Aᵢ = Activity/exam grade for semester i

## Key Topics Covered

### 1. Frequency Distribution

A **frequency distribution** is a table that shows classes or intervals of data with a count of the number of entries in each class. It's fundamental for understanding data patterns and is the foundation for creating histograms.

#### Components:
- **Class limits**: Lower and upper boundaries of each class
- **Class size**: The width of each class interval
- **Frequency (f)**: Number of data entries in each class
- **Relative frequency**: Proportion of data in each class (f/n)
- **Cumulative frequency**: Sum of frequencies up to a given class

#### Construction Steps:
1. Decide the number of classes (typically 5-20)
2. Calculate class size: (max - min) / number of classes
3. Determine class limits
4. Count frequencies for each class
5. Calculate additional measures (relative, cumulative frequencies)

### 2. Histograms and Their Relationship to Frequency Distributions

**Histograms are vectorially related to frequency distributions** - they are the graphical representation of frequency distribution tables.

#### Key Characteristics:
- **Bar chart** representing frequency distribution
- **Horizontal axis**: Quantitative data values (class boundaries)
- **Vertical axis**: Frequencies or relative frequencies
- **Consecutive bars must touch** (unlike regular bar charts)
- **Class boundaries**: Numbers that separate classes without gaps

#### Types of Histograms:
1. **Frequency Histogram**: Shows absolute frequencies
2. **Relative Frequency Histogram**: Shows proportions/percentages
3. **Frequency Polygon**: Line graph emphasizing continuous change

### 3. Outliers in Histograms

**Outliers, by definition, have few values** and can represent various phenomena:

#### What Outliers May Indicate:
- **Data entry errors** (typing mistakes)
- **Measurement errors**
- **Fraudulent activities**
- **Genuine extreme values**
- **Equipment malfunctions**

#### Impact on Histograms:
- **Generate few bars** (sparse representation)
- **Create gaps** in the distribution
- **Skew the overall pattern**
- **Affect central tendency measures**
- **May require special handling** in analysis

#### Outlier Detection in Histograms:
- Visible as **isolated bars** far from main distribution
- **Large gaps** between bars
- **Extremely tall or short bars** at distribution extremes
- **Asymmetric patterns** in otherwise normal distributions

### 4. Distribution Shapes

Understanding distribution shapes helps identify data characteristics:

#### Symmetric Distribution:
- Mean ≈ Median ≈ Mode
- Bell-shaped or uniform patterns
- Equal spread on both sides

#### Left-Skewed (Negatively Skewed):
- Mean < Median < Mode
- Tail extends to the left
- Few extremely low values

#### Right-Skewed (Positively Skewed):
- Mode < Median < Mean
- Tail extends to the right
- Few extremely high values

#### Uniform Distribution:
- All classes have equal frequencies
- Rectangular shape in histogram

### 5. Central Tendency Measures

#### Mean (μ or x̄):
- Sum of all values divided by count
- Most affected by outliers
- Uses all data points

#### Median:
- Middle value when data is ordered
- Less affected by outliers
- Robust measure

#### Mode:
- Most frequently occurring value
- May not exist or may be multiple
- Good for categorical data

### 6. Practical Applications

#### Data Mining Context:
- **Pattern Recognition**: Identifying data distributions
- **Anomaly Detection**: Finding outliers
- **Data Quality Assessment**: Checking for errors
- **Feature Engineering**: Understanding variable distributions
- **Model Selection**: Choosing appropriate algorithms based on data distribution

#### Python Implementation Examples:
```python
import matplotlib.pyplot as plt
import numpy as np

# Create frequency distribution
def create_frequency_distribution(data, num_classes=7):
    min_val, max_val = min(data), max(data)
    class_size = (max_val - min_val) / num_classes
    
    # Define class boundaries
    boundaries = [min_val + i * class_size for i in range(num_classes + 1)]
    
    # Count frequencies
    frequencies = []
    for i in range(num_classes):
        count = sum(1 for x in data if boundaries[i] <= x < boundaries[i+1])
        frequencies.append(count)
    
    return boundaries, frequencies

# Create histogram
def plot_histogram(data, title="Frequency Distribution"):
    plt.figure(figsize=(10, 6))
    plt.hist(data, bins=7, edgecolor='black', alpha=0.7)
    plt.title(title)
    plt.xlabel('Values')
    plt.ylabel('Frequency')
    plt.grid(True, alpha=0.3)
    plt.show()
```

## Bibliography

### Primary References:
1. **Castro, L. N. & Ferrari, D. G.** (2016). *Introdução à mineração de dados: conceitos básicos, algoritmos e aplicações*. Saraiva.

2. **Ferreira, A. C. P. L. et al.** (2024). *Inteligência Artificial - Uma Abordagem de Aprendizado de Máquina*. 2nd Ed. LTC.

3. **Larson & Farber** (2015). *Estatística Aplicada*. Pearson.

## Repository Structure

```
├── data/                 # Sample datasets
├── notebooks/           # Jupyter notebooks with examples
├── scripts/             # Python scripts for analysis
├── images/              # Generated plots and visualizations
└── docs/                # Additional documentation
```

## Getting Started

### Prerequisites:
- Python 3.7+
- Required libraries: pandas, numpy, matplotlib, seaborn, scikit-learn

### Installation:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### Quick Start:
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

# Load sample data
data = [50, 40, 41, 17, 11, 7, 22, 44, 28, 21, 19, 23, 37, 51, 54, 42, 86,
        41, 78, 56, 72, 56, 17, 7, 69, 30, 80, 56, 29, 33, 46, 31, 39, 20,
        18, 29, 34, 59, 73, 77, 36, 39, 30, 62, 54, 67, 39, 31, 53, 44]

# Create histogram
plt.figure(figsize=(10, 6))
plt.hist(data, bins=7, edgecolor='black')
plt.title('Internet Usage Distribution')
plt.xlabel('Minutes Online')
plt.ylabel('Frequency')
plt.show()

# Calculate statistics
print(f"Mean: {np.mean(data):.2f}")
print(f"Median: {np.median(data):.2f}")
print(f"Standard Deviation: {np.std(data):.2f}")
```

## Key Learning Outcomes

After completing this course, students will be able to:

1. **Construct and interpret frequency distributions** from raw data
2. **Create various types of histograms** and understand their relationship to frequency distributions
3. **Identify and handle outliers** in datasets
4. **Analyze distribution shapes** and their implications
5. **Calculate and interpret central tendency measures**
6. **Apply statistical concepts** to data mining problems
7. **Use Python tools** for statistical analysis and visualization

## Important Notes

- **Outliers require careful consideration** - they may represent valuable insights or data quality issues
- **Histogram bins should be chosen thoughtfully** - too few may hide patterns, too many may create noise
- **Frequency distributions are fundamental** to understanding data structure before applying advanced data mining techniques
- **Visual analysis complements numerical statistics** for comprehensive data understanding


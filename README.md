

<br>


#  <p align="center"> [Specialized Consulting for Integrated Project: Data Mining]()


<br><br>

#### <p align="center"> [![Sponsor Quantum Software Development](https://img.shields.io/badge/Sponsor-Quantum%20Software%20Development-brightgreen?logo=GitHub)](https://github.com/sponsors/Quantum-Software-Development)


<br><br>


[**Institution:**]() Pontifical Catholic University of São Paulo (PUC-SP)  
[**School:**]() Faculty of Interdisciplinary Studies  
[**Program:**]() Humanistic AI and Data Science
[**Semester:**]() 2nd Semester 2025  
Professor:  [Daniel Rodrigues da Silva]()  

<br><br>


## ⚠️ [Important Notes]()


- [Whenever possible](), projects and deliverables developed during the course will be made [publicly accessible]().

- The course emphasizes [**practical, hands-on experience**]() with real datasets to emulate professional consulting scenarios in the field of Data Mining.

- All activities and materials will strictly adhere to the [**academic and ethical guidelines of PUC-SP**](). Any content not authorized for public disclosure will remain [**confidential**]() and stored in [private repositories]().




<br><br>


## Table of Contents

<br>


1. [Course Overview](#course-overview)
2. [Objectives](#objectives)
3. [Syllabus](#syllabus)
4. [Weekly Schedule](#weekly-schedule)
5. [Tools and Technologies](#tools-and-technologies)
6. [Installation and Setup](#installation-and-setup)
7. [Assessment](#assessment)
8. [Bibliography](#bibliography)
   - [Basic Bibliography](#basic-bibliography)
   - [Complementary Bibliography](#complementary-bibliography)
9. [Notes](#notes)


<br><br>


##  [Course Overview]()

<br>


This course introduces [**data mining techniques**]() with a focus on [**unsupervised learning methods**](), including:

- Clustering algorithms (K-Means, Affinity Propagation, Mean-Shift)
- Principal Component Analysis (PCA)
- Dictionary Learning
- Novelty and outlier detection

Students will work on [**practical projects**]() inspired by real-world problem-solving in third-sector organizations. Final deliverables will be shared in **open repositories** and made available to the broader community, schools, libraries, and non-profits.


<br><br>


## [Objectives]()

Enable students to **plan, conduct, and complete a research project** applying key **data mining concepts, algorithms, and methodologies**.

<br><br>


## [Syllabus]()

<br>

- Fundamentals of Data Mining
- Data cleaning and preparation
- Predictive analysis
- Clustering methods (K-Means, Affinity Propagation, Mean-Shift)
- Principal Component Analysis (PCA)
- Dictionary Learning
- Novelty and outlier detection
- Application of concepts to real-world consulting scenarios


<br><br>


##  [Weekly Schedule]()

<br>

| [Week]() | [Topic]() | [Methodology]() | [Tools]() |
|------|-------|-------------|-------|
| 1 | Course introduction | Active methodology | – |
| 2–3 | Review of statistical methods | Active methodology | Python |
| 4 | Fundamentals of Data Mining | Active methodology | Python |
| 5–6 | Data cleaning and preparation | Active methodology | Python |
| 7 | Predictive analysis | Active methodology | Python |
| 8, 10 | Clustering techniques | Active methodology | Python |
| 9 | **P1 Exam** | Written (Individual) | – |
| 11 | K-Means algorithm | Active methodology | Python |
| 12 | Affinity Propagation | Active methodology | Python |
| 13 | Mean-Shift algorithm | Active methodology | Python |
| 14 | Principal Component Analysis (PCA) | Active methodology | Python |
| 15 | Dictionary Learning | Active methodology | Python |
| 16 | **P2 Exam** | Written (Individual) | – |
| 17 | **P3 Exam & Grade Closure** | Written (Individual) | – |
| 18 | Final grade submission | – | – |


<br><br>


##  [Tools and Technologies]()

<br>

- **Programming Language:** Python  
- **Libraries:** NumPy, Pandas, Scikit-learn, Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook or other Python IDEs



<br><br>



##  Installation and Setup

<br>

Follow these steps to set up your local environment for the course projects:

<br>

[1](). **Clone the repository**


```
git clone https://github.com/<username>/<repository-name>.git
cd <repository-name>
```


<br>


[2](). **Create a virtual environment** (recommended)


```
python -m venv venv
source venv/bin/activate   \# Mac/Linux
venv\Scripts\activate      \# Windows
```


<br>


[3](). **Install dependencies**
Make sure `pip` is updated:
```

pip install --upgrade pip

```
Then install the required packages:
```

pip install -r requirements.txt

```
*(If `requirements.txt` is not provided, install manually:)*  
```

pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```


<br>


[4](). **Run Jupyter Notebook**
   
```
jupyter notebook
```


<br>


[5](). **Open course notebooks** and start practicing.



<br><br>


##  [Assessment]()

<br>


| Exam | Date | Format | Weight |
|------|------|--------|--------|
| **P1** | 01/10/2025 | Written – Individual | Arithmetic mean |
| **P2** | 19/11/2025 | Written – Individual | Arithmetic mean |
| **P3** | Substitution exam | Written – Individual | Replaces lowest score |

<br>

[**Final Grade:**]() Arithmetic mean of assessments.


<br><br>

# I - [class_1- Introduction - Data Mining With Python]()

<br>

☞ [Access Booklet](https://github.com/Quantum-Software-Development/specialized-consulting-data-mining/blob/81e2951f73c87cf7c4396a36d48be92384b7b720/class_1-%20Introduction%20-%20Data%20Mining%20With%20Python/Book%20-%20Introd%20to%20Data%20Mining%20With%20Python.pdf)


<br>

## [Example 1]()

<br>


The following sample lists the number of minutes that 60 cable TV users watched content from their package in the last two hours. Construct a frequency distribution with 8 classes and build a histogram.

<br>


[Data]():

```
20, 55, 5, 64, 78, 49, 91, 87, 18, 83, 33, 39, 30, 31, 59, 85, 102, 24, 27, 28,
92, 108, 98, 67, 85, 109, 48, 19, 32, 69, 24, 59, 6, 49, 116, 37, 92, 43, 101, 60,
55, 107, 25, 33, 57, 25, 17, 49, 24, 101, 14, 45, 73, 120, 91, 2, 11, 47, 21, 38
```

<br><br>


### [Step 1](): Determine Range and Number of Classes

- Minimum value: 2
- Maximum value: 120
- Number of classes ($k$): 8 (given)


<br><br>


### [Step 2](): Calculate Class Width


<br><br>

$$
\huge
w = \left\lceil \frac{\text{max} - \text{min}}{k} \right\rceil = \left\lceil \frac{120 - 2}{8} \right\rceil = 15
$$


<br><br>

### [Step 3](): Construct Class Intervals (from minimum value)

| Class Interval | Explanation |
| :-- | :-- |
| 2 - 16 | Starts from minimum 2 |
| 17 - 31 | 16 + 1 to 31 |
| 32 - 46 | Next range |
| 47 - 61 | Next range |
| 62 - 76 | Next range |
| 77 - 91 | Next range |
| 92 - 106 | Next range |
| 107 - 121 | Covers maximum 120 |

<br>

### [Step 4](): Frequency Distribution Table

<br>

| Class Interval | Frequency |
| :--: | :--: |
| 2 - 16 | 5 |
| 17 - 31 | 14 |
| 32 - 46 | 8 |
| 47 - 61 | 13 |
| 62 - 76 | 5 |
| 77 - 91 | 8 |
| 92 - 106 | 6 |
| 107 - 121 | 5 |


<br><br>


### [Step 5](): Calculate Midpoints for Each Class

<br>

$$
\Huge
x_i = \frac{\text{Lower limit} + \text{Upper limit}}{2}
$$

<br><br>

| Class Interval | Midpoint ($x_i$) |
| :-- | :-- |
| 2 - 16 | 9 |
| 17 - 31 | 24 |
| 32 - 46 | 39 |
| 47 - 61 | 54 |
| 62 - 76 | 69 |
| 77 - 91 | 84 |
| 92 - 106 | 99 |
| 107 - 121 | 114 |

<br><br>


### [Step 6](): Calculate Mean Using Frequency and Midpoints

<br>

### [Mean](): ($\bar{x}$) is calculated by:

<br><br>

$$
\Huge
\bar{x} = \frac{\sum f_i x_i}{\sum f_i}
$$

<br><br>

### [Where](): $f_i$ = frequency, $x_i$ = [Midpoint]().


<br>

### [Calculate each product]():

<br>

| Class Interval | $f_i$ | $x_i$ | $f_i \times x_i$ |
| :-- | :-- | :-- | :-- |
| 2 - 16 | 5 | 9 | 45 |
| 17 - 31 | 14 | 24 | 336 |
| 32 - 46 | 8 | 39 | 312 |
| 47 - 61 | 13 | 54 | 702 |
| 62 - 76 | 5 | 69 | 345 |
| 77 - 91 | 8 | 84 | 672 |
| 92 - 106 | 6 | 99 | 594 |
| 107 - 121 | 5 | 114 | 570 |

<br>

### [Sum frequencies](): $5 + 14 + 8 + 13 + 5 + 8 + 6 + 5$ = [64]()

### [Sum of products](): $45 + 336 + 312 + 702 + 345 + 672 + 594 + 570$ = [3576]()

<br>

### [Calculate mean]():

<br><br>

$$
\huge
\bar{x} = \frac{3576}{64} = 55.875
$$

<br><br>


### [Step 7](): Histogram, Bar Plot and Time Series Frequency Distribution Over Time

- Construct a histogram, bar plot and  Time Series  with class intervals on the x-axis and frequencies on the y-axis.
- Each bar height corresponds to the frequency of the class.


<br>

☞ [Access Code](https://github.com/Quantum-Software-Development/specialized-consulting-data-mining/blob/a61b0572e5bca4d6f06b0187722f8ef97214c0a4/class_1-%20Introduction%20-%20Data%20Mining%20With%20Python/Code/DataMining_1.ipynb)

☞ [Access Dataset](https://github.com/Quantum-Software-Development/specialized-consulting-data-mining/blob/01b6e27e588c3b830561385f14bd0d246f55049d/class_1-%20Introduction%20-%20Data%20Mining%20With%20Python/Banks%20Dataset/banco.csv)

☞ [Access Plots](https://github.com/Quantum-Software-Development/specialized-consulting-data-mining/tree/a61b0572e5bca4d6f06b0187722f8ef97214c0a4/class_1-%20Introduction%20-%20Data%20Mining%20With%20Python/Plots)


<br><br>

###[Frequency Analysis and Time Series Visualization]()

This notebook demonstrates how to perform frequency analysis on a CSV dataset, visualize results with histograms and bar plots, and create a time series chart using Python.

<br>

###  [1](). Install and Import Libraries

```python
# Import required libraries
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
```

<br>

###  [2](). Load Dataset

```python
# Load CSV file (semicolon-separated)
df = pd.read_csv('chose your dataset', sep=';')

# Select only the "day" column
df1 = df['day']
```

<br>

###  [3](). Calculate Frequencies


```python
# Calculate absolute frequency (ascending order)
freq_abs = pd.Series(df1).value_counts(ascending=True)

# Calculate relative frequency (normalized, 3 decimal places)
freq_rel = pd.Series(df1).value_counts(normalize=True).round(3)

# Create a DataFrame with both measures
df_freq = pd.DataFrame({
    'Absolute Frequency': freq_abs,
    'Relative Frequency': freq_rel
})

# Display the frequency table
display(df_freq)
```

<br>

###  [4]() 🌙 Histogram (Dark Theme)

```python
# Create figure and axes with dark background
plt.style.use('seaborn-v0_8-darkgrid')
fig, ax = plt.subplots(figsize=(16, 4))
fig.patch.set_facecolor('black')
ax.set_facecolor('black')

# Plot histogram
sns.histplot(df1, color='turquoise', ax=ax)

# Customize labels and ticks
plt.xlabel("Values")
plt.ylabel("Frequency")
plt.title("Frequency Distribution", color='white')
plt.tick_params(axis='x', colors='white')
plt.tick_params(axis='y', colors='white')

# Show plot
plt.show()
```
























































<br><br>
<br><br>
<br><br>
<br><br>
<br><br>
<br><br>




##  [Bibliography]()

<br>

### [Basic Bibliography]()

- CASTRO, L. N. *Introdução a mineração de dados: conceitos básicos, algoritmos e aplicações*. Saraiva, 2016.  
- PIRIM, H. *Recent Applications in Data Clustering*. IntechOpen, 2018.  
- SEN, J. *Machine Learning: Artificial Intelligence*. IntechOpen, 2021.

<br>

### [Complementary Bibliography]()

- THOMAS, C. *Data Mining*. IntechOpen, 2018.  
- HUTTER, F.; KOTTHOFF, L.; VANSCHOREN, J. *Automated Machine Learning: Methods, Systems, Challenges*. Springer Nature, 2019.  
- NETTO, A.; MACIEL, F. *Python para Data Science e Machine Learning Descomplicado*. Alta Books, 2021.  
- RUSSELL, S. J.; NORVIG, P. *Artificial Intelligence: A Modern Approach*. GEN LTC, 2022.  
- SUD, K.; ERDOGMUS, P.; KADRY, S. *Introduction to Data Science and Machine Learning*. IntechOpen, 2020.



<br><br>


## 💌 [Let the data flow... Ping Me !](mailto:fabicampanari@proton.me)

<br><br>



#### <p align="center">  🛸๋ My Contacts [Hub](https://linktr.ee/fabianacampanari)


<br>

### <p align="center"> <img src="https://github.com/user-attachments/assets/517fc573-7607-4c5d-82a7-38383cc0537d" />




<br><br><br>

<p align="center">  ────────────── 🔭⋆ ──────────────


<p align="center"> ➣➢➤ <a href="#top">Back to Top </a>

<!--
<p align="center">  ────────────── ✦ ──────────────
-->



<!-- Programmers and artists are the only professionals whose hobby is their profession."

" I love people who are committed to transforming the world "

" I'm big fan of those who are making waves in the world! "

##### <p align="center">( Rafael Lain ) </p>   -->

#

###### <p align="center"> Copyright 2025 Quantum Software Development. Code released under the [MIT License license.](https://github.com/Quantum-Software-Development/Math/blob/3bf8270ca09d3848f2bf22f9ac89368e52a2fb66/LICENSE)

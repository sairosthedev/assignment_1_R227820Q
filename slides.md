---
theme: dracula
title: Data Pre-processing Major Tasks
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
fonts:
  sans: 'Lato'
  serif: 'Lato'
  mono: 'Fira Code'
---

# Data Pre-processing: Major Tasks

<div style="font-size:1.3em; margin-top: 2em;">
Data pre-processing is the foundation for effective data analysis and mining. It transforms raw, messy data into a clean, integrated, and structured format, ensuring quality and consistency for reliable insights.
</div>

<div style="margin-top: 2.5em; font-size:1.1em;">
<strong>Macdonald Sairos</strong> &nbsp;|&nbsp; <strong>Reg Number:</strong> R227820Q
</div>

---

# What is Data Pre-processing?

Data pre-processing is a crucial step in data mining and machine learning. It involves transforming raw data into a clean and usable format, ensuring data quality, consistency, and reliability for analysis. The main tasks are Data Cleaning, Data Integration, Data Reduction, Data Transformation, and Data Discretization.

---

# a. Data Cleaning

<div class="grid grid-cols-2 gap-4">
<div>
Data cleaning addresses incomplete, noisy, or inconsistent data by systematically identifying and resolving quality issues. It ensures the reliability of data for analysis and decision-making.
<ul>
<li>Fill missing values (mean, constant, inference)</li>
<li>Detect and handle outliers</li>
<li>Smooth noisy data (binning, regression)</li>
<li>Correct inconsistencies</li>
</ul>
</div>
<div>
<strong>Why it matters:</strong>
<ul>
<li>Improves data quality</li>
<li>Reduces errors in analysis</li>
<li>Essential for both OLAP and data mining</li>
</ul>
</div>
</div>

---

# Data Cleaning Example (Python)

```python
import pandas as pd
# Fill missing values with the mean
cleaned = df.fillna(df.mean())
# Remove outliers using z-score
from scipy import stats
df = df[(np.abs(stats.zscore(df)) < 3).all(axis=1)]
```

---

# b. Data Integration

<div class="grid grid-cols-2 gap-4">
<div>
Data integration combines data from multiple sources into a unified, consistent view. This is essential for data warehousing and mining.
<ul>
<li>Schema integration and object matching</li>
<li>Redundancy detection and removal</li>
<li>Resolve data value conflicts</li>
</ul>
</div>
<div>
<strong>Key points:</strong>
<ul>
<li>Careful attribute mapping</li>
<li>Correlation analysis for redundancy</li>
<li>Improves consistency and quality</li>
</ul>
</div>
</div>

---

# c. Data Reduction

<div class="grid grid-cols-2 gap-4">
<div>
Data reduction decreases the volume of data while maintaining its analytical integrity, enabling faster processing and easier visualization.
<ul>
<li>Aggregation (data cubes)</li>
<li>Attribute/feature selection</li>
<li>Dimensionality reduction (PCA)</li>
<li>Numerosity reduction (sampling, clustering)</li>
</ul>
</div>
<div>
<strong>Benefits:</strong>
<ul>
<li>Speeds up mining</li>
<li>Reduces storage costs</li>
<li>Makes patterns easier to interpret</li>
</ul>
</div>
</div>

---

# d. Data Transformation

<div class="grid grid-cols-2 gap-4">
<div>
Data transformation converts data into forms suitable for mining, improving analysis quality and mining results.
<ul>
<li>Smoothing (removing noise)</li>
<li>Aggregation (summarizing data)</li>
<li>Generalization (concept hierarchies)</li>
<li>Normalization (scaling values)</li>
</ul>
</div>
<div>
<strong>Why transform?</strong>
<ul>
<li>Prepares data for algorithms</li>
<li>Improves comparability</li>
<li>Enables multi-level analysis</li>
</ul>
</div>
</div>

---

# Data Transformation Example (Python)

```python
from sklearn.preprocessing import MinMaxScaler
# Normalize data to [0, 1] range
scaler = MinMaxScaler()
df_scaled = scaler.fit_transform(df)
```

---

# e. Data Discretization

<div class="grid grid-cols-2 gap-4">
<div>
Data discretization transforms continuous attributes into discrete intervals or categories, reducing complexity and enabling certain algorithms to function properly.
<ul>
<li>Binning (equal-width/depth)</li>
<li>Histogram analysis</li>
<li>Clustering-based methods</li>
<li>Entropy-based partitioning</li>
</ul>
</div>
<div>
<strong>Advantages:</strong>
<ul>
<li>Supports categorical algorithms</li>
<li>Simplifies interpretation</li>
<li>Enables concept hierarchies</li>
</ul>
</div>
</div>

---

# Real-World Examples

<div class="grid grid-cols-2 gap-4">
<div>
<strong>Healthcare:</strong>
<ul>
<li>Cleaning: Handling missing patient records</li>
<li>Integration: Combining lab and clinical data</li>
<li>Reduction: Selecting key biomarkers</li>
</ul>
<strong>Finance:</strong>
<ul>
<li>Cleaning: Removing duplicate transactions</li>
<li>Transformation: Normalizing credit scores</li>
</ul>
</div>
<div>
<strong>Retail:</strong>
<ul>
<li>Integration: Merging online and in-store sales</li>
<li>Discretization: Grouping customers by age range</li>
</ul>
<strong>IoT/Sensors:</strong>
<ul>
<li>Reduction: Aggregating sensor readings hourly</li>
<li>Cleaning: Filtering out sensor noise</li>
</ul>
</div>
</div>

---

# Summary

<div class="grid grid-cols-2 gap-4">
<div>
Data pre-processing ensures data quality and usability through five major interconnected tasks, essential for effective data mining and machine learning.
<ul>
<li>Higher quality input data</li>
<li>More reliable analysis results</li>
<li>Efficient mining processes</li>
</ul>
</div>
<div>
<ul>
<li>Better pattern discovery</li>
<li>Improved decision support</li>
<li>Foundation for advanced analytics</li>
</ul>
</div>
</div>








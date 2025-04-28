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

Data pre-processing is a crucial step in data mining and machine learning. It involves transforming raw data into a clean and usable format, ensuring data quality, consistency, and reliability for analysis. 

<div class="grid grid-cols-2 gap-4">
<div>
<strong>Definition:</strong>
<ul>
<li>Prepares raw, messy, or incomplete data for analysis.</li>
<li>Removes errors, inconsistencies, and redundancies.</li>
<li>Transforms data into a structured and standardized format.</li>
</ul>
</div>
<div>
<strong>Why is it important?</strong>
<ul>
<li>Ensures high-quality input for data mining and machine learning models.</li>
<li>Improves accuracy, efficiency, and interpretability of results.</li>
<li>Reduces bias and prevents misleading conclusions.</li>
</ul>
</div>
</div>

The main tasks are Data Cleaning, Data Integration, Data Reduction, Data Transformation, and Data Discretization. Each task addresses specific challenges in preparing data for effective analysis and decision-making.

---

# a. Data Cleaning

<div class="grid grid-cols-2 gap-4">
<div>
Data cleaning is the process of detecting and correcting (or removing) corrupt or inaccurate records from a dataset. It addresses issues such as missing values, noise, and inconsistencies, which are common in real-world data. Clean data is essential for accurate analysis and reliable results.
<ul>
<li><strong>Missing values:</strong> Can be filled using mean, median, mode, or inferred values.</li>
<li><strong>Outlier detection:</strong> Identifies unusual data points that may distort analysis.</li>
<li><strong>Noisy data:</strong> Smoothed using binning, regression, or clustering.</li>
<li><strong>Inconsistencies:</strong> Corrected through manual or automated routines.</li>
</ul>
</div>
<div>
<strong>Why it matters:</strong>
<ul>
<li>Improves data quality and trustworthiness.</li>
<li>Reduces errors and bias in analysis.</li>
<li>Ensures valid input for OLAP and data mining.</li>
<li>Supports regulatory compliance and data governance.</li>
</ul>
<p><strong>Example:</strong> In healthcare, missing patient ages can be filled with the average age for similar cases, and outliers in lab results can be flagged for review.</p>
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
import numpy as np
df = df[(np.abs(stats.zscore(df.select_dtypes(include=[np.number]))) < 3).all(axis=1)]
```

---

# b. Data Integration

<div class="grid grid-cols-2 gap-4">
<div>
Data integration is the process of combining data from different sources to provide a unified view. This is crucial for organizations that store data in multiple databases, files, or formats. Integration ensures consistency and completeness across datasets.
<ul>
<li><strong>Schema integration:</strong> Aligns different data structures and resolves naming conflicts.</li>
<li><strong>Entity identification:</strong> Matches records that refer to the same real-world entity.</li>
<li><strong>Redundancy detection:</strong> Identifies and removes duplicate or derivable data.</li>
<li><strong>Data value conflicts:</strong> Resolves differences in data representation (e.g., units, formats).</li>
</ul>
</div>
<div>
<strong>Key points:</strong>
<ul>
<li>Requires careful attribute mapping and metadata management.</li>
<li>Improves data consistency, quality, and usability.</li>
<li>Facilitates comprehensive analysis and reporting.</li>
<li>Supports data warehousing and business intelligence.</li>
</ul>
<p><strong>Example:</strong> Merging customer data from sales and support databases, ensuring that "customer_id" and "client_number" refer to the same entity.</p>
</div>
</div>

---

# c. Data Reduction

<div class="grid grid-cols-2 gap-4">
<div>
Data reduction aims to reduce the volume of data while preserving its analytical value. This is vital for handling large datasets efficiently and making analysis feasible.
<ul>
<li><strong>Aggregation:</strong> Summarizes data (e.g., daily to monthly sales).</li>
<li><strong>Attribute selection:</strong> Removes irrelevant or redundant features.</li>
<li><strong>Dimensionality reduction:</strong> Uses techniques like PCA to reduce variables.</li>
<li><strong>Numerosity reduction:</strong> Applies models, sampling, or clustering to represent data compactly.</li>
</ul>
</div>
<div>
<strong>Benefits:</strong>
<ul>
<li>Speeds up data mining and analysis.</li>
<li>Reduces storage and computation costs.</li>
<li>Makes patterns and trends easier to interpret.</li>
<li>Improves visualization and reporting.</li>
</ul>
<p><strong>Example:</strong> Using PCA to reduce hundreds of sensor readings to a few principal components for anomaly detection.</p>
</div>
</div>

---

# d. Data Transformation

<div class="grid grid-cols-2 gap-4">
<div>
Data transformation converts data into formats suitable for analysis and mining. It enhances data quality and enables more effective pattern discovery.
<ul>
<li><strong>Smoothing:</strong> Removes noise from data (e.g., moving averages).</li>
<li><strong>Aggregation:</strong> Summarizes data at higher levels (e.g., total sales per region).</li>
<li><strong>Generalization:</strong> Replaces detailed data with higher-level concepts (e.g., age groups).</li>
<li><strong>Normalization:</strong> Scales values to a common range for comparability.</li>
</ul>
</div>
<div>
<strong>Why transform?</strong>
<ul>
<li>Prepares data for machine learning algorithms.</li>
<li>Improves comparability and interpretability.</li>
<li>Enables multi-level and hierarchical analysis.</li>
<li>Supports feature engineering for better models.</li>
</ul>
<p><strong>Example:</strong> Normalizing income data to a 0-1 scale before clustering customers.</p>
</div>
</div>

---

# Data Pre-processing Code Examples (Python)

<div class="grid grid-cols-2 gap-4">
<div>
<strong>Data Transformation (Normalization):</strong>

```python
from sklearn.preprocessing import MinMaxScaler
# Normalize data to [0, 1] range
scaler = MinMaxScaler()
df_scaled = scaler.fit_transform(df)
```

<strong>Data Reduction (PCA):</strong>

```python
from sklearn.decomposition import PCA
# Reduce to 2 principal components
pca = PCA(n_components=2)
reduced = pca.fit_transform(df)
```
</div>
<div>
<strong>Data Integration (Merging DataFrames):</strong>

```python
import pandas as pd
# Merge sales and customer data using a common key
merged = pd.merge(
    sales_df,           # Sales data DataFrame
    customer_df,        # Customer data DataFrame
    left_on='customer_id',
    right_on='customer_id',
    how='inner'         # Only include matching records
)
# Result:
# merged DataFrame with unified customer and
# sales information for all matching records
```
</div>
</div>

---

# e. Data Discretization

<div class="grid grid-cols-2 gap-4">
<div>
Data discretization converts continuous variables into discrete categories or intervals. This is important for algorithms that require categorical input and for simplifying data.
<ul>
<li><strong>Binning:</strong> Groups values into intervals (equal-width or equal-depth).</li>
<li><strong>Histogram analysis:</strong> Divides data into buckets for summary statistics.</li>
<li><strong>Clustering-based:</strong> Assigns values to clusters as categories.</li>
<li><strong>Entropy-based:</strong> Uses information gain to determine split points.</li>
</ul>
</div>
<div>
<strong>Advantages:</strong>
<ul>
<li>Reduces data complexity and noise.</li>
<li>Supports categorical data mining algorithms.</li>
<li>Facilitates concept hierarchy generation.</li>
<li>Improves interpretability and pattern discovery.</li>
</ul>
<p><strong>Example:</strong> Discretizing ages into groups: 0-18 (child), 19-35 (young adult), 36-60 (adult), 61+ (senior).</p>
</div>
</div>

---

# Real-World Examples

<div class="grid grid-cols-2 gap-4">
<div>
<strong>Healthcare:</strong>
<ul>
<li>Cleaning: Handling missing patient records and correcting inconsistent lab results.</li>
<li>Integration: Combining lab, clinical, and insurance data for a holistic view.</li>
<li>Reduction: Selecting key biomarkers from thousands of test results.</li>
<li>Transformation: Aggregating patient visits by month.</li>
</ul>
<strong>Finance:</strong>
<ul>
<li>Cleaning: Removing duplicate or fraudulent transactions.</li>
<li>Integration: Merging credit and transaction histories.</li>
<li>Transformation: Normalizing credit scores for risk analysis.</li>
<li>Discretization: Grouping loan amounts into risk categories.</li>
</ul>
</div>
<div>
<strong>Retail:</strong>
<ul>
<li>Integration: Merging online and in-store sales data.</li>
<li>Reduction: Sampling customer purchase histories for trend analysis.</li>
<li>Discretization: Grouping customers by age or spending range.</li>
<li>Cleaning: Filtering out erroneous sales entries.</li>
</ul>
<strong>IoT/Sensors:</strong>
<ul>
<li>Reduction: Aggregating sensor readings hourly or daily.</li>
<li>Cleaning: Filtering out sensor noise and outliers.</li>
<li>Transformation: Converting raw voltages to temperature readings.</li>
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
<li>Reduces bias and errors in models</li>
</ul>
</div>
<div>
<ul>
<li>Better pattern discovery</li>
<li>Improved decision support</li>
<li>Foundation for advanced analytics</li>
<li>Supports regulatory and business requirements</li>
</ul>
</div>
</div>








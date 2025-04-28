---
theme: seriph
title: Data Pre-processing Major Tasks
class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Data Pre-processing: Major Tasks

<div style="font-size:1.3em; margin-top: 2em;">
Data pre-processing is the foundation for effective data analysis and mining. It transforms raw, messy data into a clean, integrated, and structured format, ensuring quality and consistency for reliable insights.
</div>

<div style="margin-top: 2.5em; font-size:1.1em;">
<strong>Macdonald Sairos</strong> &nbsp;|&nbsp; <strong>Reg Number:</strong> R227820Q
</div>

<div style="margin-top: 2.5em;">
<strong>Major Tasks:</strong><br>
<span style="display:inline-block; margin:0.5em 0;">Data Cleaning &nbsp;|&nbsp; Data Integration &nbsp;|&nbsp; Data Reduction &nbsp;|&nbsp; Data Transformation &nbsp;|&nbsp; Data Discretization</span>
</div>

---

# What is Data Pre-processing?

- Data pre-processing is a crucial step in data mining and machine learning.
- It involves transforming raw data into a clean and usable format.
- Ensures data quality, consistency, and reliability for analysis.

---

# a. Data Cleaning

- Addresses incomplete, noisy, or inconsistent data ("dirty" data).
- Key tasks:
  - Filling in missing values (e.g., ignore tuple, fill manually, use mean, or most probable value)
  - Identifying and handling outliers
  - Smoothing noisy data (e.g., binning, regression, clustering)
  - Resolving inconsistencies (e.g., naming conventions, coding errors)
- Methods for missing data: ignore, fill with constant, mean, or infer value
- Smoothing: binning, regression, clustering, concept hierarchies
- Inconsistencies: manual correction, automated routines, or during integration
- Outlier detection: statistical, distance, density, or deviation-based

---

# b. Data Integration

- Combines data from multiple sources (databases, files, cubes) into a unified view
- Required for data warehousing, OLAP, and data mining
- Issues:
  - Schema integration and object matching (entity identification)
  - Redundancy (same attribute, different names)
  - Data value conflicts (different representations/scales)
- Solutions:
  - Careful integration reduces redundancies and inconsistencies
  - Use of global schema, mapping, and correlation analysis
- Goal: Provide consistent, integrated data for quality analysis

---

# c. Data Reduction

- Reduces data volume while maintaining analytical integrity
- Strategies:
  - Data cube aggregation (summarize data at multiple levels)
  - Attribute subset selection (feature selection, dimensionality reduction)
  - Dimensionality reduction (e.g., PCA)
  - Numerosity reduction (parametric: models; non-parametric: histograms, clustering, sampling)
  - Discretization and concept hierarchy generation
- Benefits: faster mining, less storage, easier visualization

---

# d. Data Transformation

- Converts/consolidates data into forms suitable for mining
- Methods:
  - Smoothing (remove noise: binning, regression, clustering)
  - Aggregation (summarize data, e.g., daily to monthly totals)
  - Generalization (replace raw data with higher-level concepts)
  - Normalization (scale values: min-max, z-score, decimal scaling)
  - Attribute construction (create new features from existing data)
- Prepares data for analysis and improves mining results

---

# e. Data Discretization

- Converts continuous attributes into discrete intervals or categories
- Reasons:
  - Some algorithms require categorical data
  - Reduces data size and complexity
  - Facilitates concept hierarchy generation
- Methods:
  - Binning (equal-width, equal-depth)
  - Histogram analysis
  - Clustering
  - Entropy-based discretization
  - Segmentation by natural partitioning (e.g., 3-4-5 rule)
- Closely related to concept hierarchy generation for numerical/categorical data

---

# Summary

- Data pre-processing ensures data quality and usability
- Major tasks:
  - Data Cleaning: handle missing, noisy, inconsistent data
  - Data Integration: unify data from multiple sources
  - Data Reduction: reduce data size, keep essential info
  - Data Transformation: convert data for analysis
  - Data Discretization: turn continuous data into categories
- Essential for effective data mining and machine learning

---








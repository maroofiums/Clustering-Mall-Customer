# Mall Customers Segmentation

**Clustering Analysis using K-Means and DBSCAN**

## Project Overview

This project focuses on identifying **meaningful customer segments** using mall customer demographic and behavioral data. The objective is to help businesses improve **targeted marketing, customer engagement, and revenue optimization** through data-driven insights.

Two unsupervised learning algorithms — **K-Means** and **DBSCAN** — were applied and compared to understand customer behavior from different perspectives.

---

## Problem Statement

The mall had access to customer data containing **Age, Annual Income, and Spending Score**, but faced several challenges:

* Customers were not clearly segmented
* High-value customers were difficult to identify
* Outliers and unusual customer behavior were not visible

### Goal

Segment customers into meaningful groups and extract actionable business insights.

---

## Solution Approach

Unsupervised learning techniques were used in the following stages:

1. **Exploratory Data Analysis (EDA)**

   * Analyzed feature distributions
   * Observed relationships and patterns among variables

2. **K-Means Clustering**

   * Used the Elbow Method to determine optimal `k = 5`
   * Assigned customers to centroid-based clusters

3. **DBSCAN Clustering**

   * Applied density-based clustering
   * Explicitly identified noise and outliers

4. **Comparison and Interpretation**

   * Compared K-Means and DBSCAN results
   * Assigned business-friendly segment labels

---

## Methodology Workflow

```
Data Loading
   ↓
EDA and Feature Scaling
   ↓
K-Means (Elbow → Fit → Labeling)
   ↓
DBSCAN (eps and min_samples tuning)
   ↓
Cluster Profiling (Age, Income, Spending)
   ↓
Comparison and Business Insights
```

---

## K-Means Cluster Insights (5 Segments)

| Cluster | Segment Name                    | Key Characteristics                         |
| ------- | ------------------------------- | ------------------------------------------- |
| 0       | Prudent Older Shoppers          | Older customers, mid-income, moderate spend |
| 1       | High Income, High Spenders      | Young adults, high income, very high spend  |
| 2       | Young Low Income, High Spenders | Young customers, low income, high spend     |
| 3       | Average Balanced Spenders       | Mid-income, moderate spending               |
| 4       | High Income, Low Spenders       | High income, very low spending              |

**Note:**
K-Means assigns every customer to a cluster, even if they do not naturally belong to one.

---

## DBSCAN Cluster Insights (6 Clusters + Noise)

| Cluster | Segment Description                         |
| ------- | ------------------------------------------- |
| -1      | Noise / Outliers (~15%) with mixed behavior |
| 0       | Young, low income, high spenders            |
| 1       | Middle-aged, low income, low spenders       |
| 2       | Older, mid-income, moderate spenders        |
| 3       | Young, mid-income, balanced spenders        |
| 4       | High income, high spenders                  |
| 5       | High income, very low spenders              |

**Note:**
DBSCAN can isolate unusual customers instead of forcing them into clusters.

---

## K-Means vs DBSCAN Comparison

### Similarities

Both algorithms consistently identified the following customer segments:

* High income, high spenders
* Young low income, high spenders
* High income, low spenders
* Older moderate spenders

### Key Differences

| Aspect             | K-Means                    | DBSCAN                      |
| ------------------ | -------------------------- | --------------------------- |
| Number of Clusters | Fixed (k = 5)              | Automatically determined    |
| Outliers           | Forced into clusters       | Explicitly labeled as noise |
| Cluster Shape      | Assumes spherical clusters | Supports arbitrary shapes   |
| Business Usage     | Simple segmentation        | Deeper behavioral insights  |

---

## Key Business Insights

### High-Value Customers

Young to middle-aged customers with high income and high spending.
These customers are the primary revenue drivers.

### Untapped Potential

Customers with high income but low spending.
This indicates an engagement issue rather than a purchasing power issue.

### Spending Is Not Equal to Income

Young customers with low income but high spending.
This highlights the importance of trends, lifestyle, and psychology.

### Hidden Patterns

Noise points identified by DBSCAN may represent niche, emerging, or irregular customer behavior.

---

## Actionable Recommendations

### Target High Income, High Spenders

* Loyalty and rewards programs
* Exclusive product launches
* Personalized shopping experiences

### Activate High Income, Low Spenders

* Customer surveys and feedback
* Premium services and experiences
* Concierge-style offerings

### Nurture Young High Spenders

* Discount-driven and trend-based campaigns
* Student-focused offers
* Strong social media engagement

### Analyze DBSCAN Noise

* Identify new customer patterns
* Detect one-time or seasonal visitors
* Explore niche market opportunities

---

## Final Conclusion

This project demonstrates that:

* **K-Means** is effective for clear and structured customer segmentation
* **DBSCAN** provides deeper insights by identifying outliers and complex patterns
* Using both together leads to a stronger and more realistic understanding of customer behavior

**Best Practice:**
Use **K-Means for strategic segmentation** and **DBSCAN for exploratory analysis and discovery**.

---

## Technology Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

## Mentor Tip

Recruiters are not only interested in models, but in **how you think**.
This project clearly demonstrates both **analytical ability** and **business understanding**.

---

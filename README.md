# D2C Customer Churn Intelligence & Retention

## Part 2 – RFM Segmentation & Retention Strategy

---

## Project Overview

This repository contains the customer segmentation and retention strategy phase of the D2C Customer Churn Intelligence project.

The objective of this phase is to:

* Segment customers using Recency, Frequency, and Monetary (RFM) analysis.
* Identify customer groups with different retention needs.
* Prioritize retention resources under budget constraints.
* Design targeted retention strategies for each customer segment.

---

## Business Objective

Rather than applying blanket discounts across the entire customer base, the company seeks to identify which customers should receive retention investments and what type of intervention is most appropriate for each customer group.

---

## Repository Structure

```text
.
├── notebooks/
│   └── rfm_segmentation.ipynb
│
├── outputs/
│   ├── segment_profile.csv
│   ├── segments.csv
│   ├── top_priority_customers.csv
│   └── segment_profile_chart.png
│
├── reports/
│   ├── retention_strategy.md
│   └── manual_review_cases.md
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Dataset

The analysis uses:

* customers.csv
* churn_labels.csv
* rfm_modeling_snapshot.csv

The RFM snapshot dataset contains leakage-safe customer-level features generated using information available up to the project snapshot date.

---

## Methodology

### 1. RFM Analysis

Customers were evaluated using:

* Recency (time since last purchase)
* Frequency (purchase count)
* Monetary Value (customer spend)

### 2. RFM Scoring

* Recency scored using quintiles
* Monetary scored using quintiles
* Frequency scored using business-driven thresholds due to discrete purchase distributions

### 3. Segment Creation

Customers were assigned into six business segments:

| Segment             | Customers |
| ------------------- | --------: |
| Champions           |       260 |
| Loyal Customers     |       523 |
| Potential Loyalists |       434 |
| At Risk             |       398 |
| Needs Attention     |       232 |
| Hibernating         |       553 |

---

## Key Findings

### Champions

* Highest value customers
* Most engaged customers
* Require loyalty protection strategies

### Loyal Customers

* Consistent repeat purchasers
* Strong retention candidates

### Potential Loyalists

* Recent purchasers
* High growth potential

### At Risk

* Previously valuable customers
* Showing signs of disengagement
* Highest retention priority

### Needs Attention

* Moderate engagement
* Require monitoring

### Hibernating

* Low engagement
* Low-value reactivation candidates

---

## Retention Priority Framework

| Priority | Segment             |
| -------- | ------------------- |
| 1        | At Risk             |
| 2        | Potential Loyalists |
| 3        | Loyal Customers     |
| 4        | Champions           |
| 5        | Needs Attention     |
| 6        | Hibernating         |

The prioritization framework was designed to maximize retention ROI under limited retention budgets.

---

## Outputs

### Analytics Outputs

* segments.csv
* segment_profile.csv
* top_priority_customers.csv

### Reports

* retention_strategy.md
* manual_review_cases.md

### Visualization

* segment_profile_chart.png

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Conclusion

RFM segmentation identified six distinct customer groups with different retention requirements. The analysis indicates that retention investments should focus primarily on At Risk customers and Potential Loyalists, while Champions should be protected through loyalty initiatives and Hibernating customers should receive only low-cost reactivation efforts.

# Bank customer analytics using clustering methods

This project builds a comprehensive customer segmentation framework by combining two approaches:

1) **Behavioral Clustering** — groups clients based on employment stability, credit activity, and delinquency patterns.
2) **RMF Segmentation** — evaluates customer value and credit behavior using quantile‑based scoring.

These methods create a view of customer profiles, enabling targeted risk management, marketing strategies, and portfolio optimization.

---

## Overview

The goal of this project is to identify distinct customer types within a credit portfolio by analyzing client features:

- credit usage intensity  
- payment behavior and delinquency patterns  
- employment characteristics  
- recency and frequency of credit applications  
- and other 

The final output consists of **five behavioral clusters** and **five RMF bins**, each with an interpretable client portrait.

---

## Key Features

### **1. Data Preparation and Analysis**

- the data can be found by the link: https://docs.yandex.ru/docs/view?url=ya-disk-public%3A%2F%2Fi%2FfCz9oIxedlBoPvvEHViJerzhVa17o161QfiiZa6880kEitZ%2B9RUOkW2UiV5uoVq%2FJ6bpmRyOJonT3VoXnDag%3D%3D%3A%2FHW1_var_8.csv&name=HW1_var_8.csv
- the raw data was cleaned
- missing data was deleted or filled with mode for categorical and median for numerical data
- each categorical feature was one-hot encoded
- distibution of each variable was plotted in columns and with boxplots, then analysed
- correlation between features was analized using correlation matrix
- the right number of clusters was chosen by assessing the Elbow, Silhouette and Davies-Bouldin methods grpahs, 5 seemed to be the best choice
- for clustering we used:
-- 1) K-Means to identify the cluster centers and regression tree to find out the most important separating features
-- 2) RMF analysis


### **2) Behavioral Clustering**
Unsupervised clustering identifies client groups based on real credit behavior:

- **Cluster 1 — Stable, low‑risk borrowers with low activity**
- **Cluster 2 — Active, experienced borrowers with moderate risk**
- **Cluster 3 — Credit‑seeking borrowers with emerging risk**
- **Cluster 4 — Conservative, low‑risk borrowers with low credit need**
- **Cluster 5 — High‑risk borrowers with delinquency patterns**

Each cluster includes a detailed portrait describing employment type, credit activity, delinquency levels, and application behavior.

---

### **3) RMF Segmentation**
Quantile‑based scoring of Recency, Monetary, and Frequency produces 93 micro‑segments, later consolidated into 5 macro‑bins:

- **Bin 1 — Churn / Low Value (RMF 111)**
- **Bin 2 — Stable / Low‑Medium Value (RMF 232)**
- **Bin 3 — Growth / Medium Value (RMF 433)**
- **Bin 4 — Core / High Value (RMF 243)**
- **Bin 5 — VIP / Top Value (RMF 555)**

Each bin includes a financial portrait: DTI, recency, credit usage, payment volume, and risk indicators.

## Possbile Applications

- Identifying VIP high‑value clients  
- Detecting emerging‑risk borrowers  
- Targeting stable customers for cross‑sell  
- Monitoring churn‑risk segments  
- Designing differentiated credit strategies 


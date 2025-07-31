
# Week 10: Unsupervised Learning 

This repository contains implementations of unsupervised learning techniques and association rule mining, applied to both numerical and mixed-type datasets.

---

## Objectives

- Identify latent patterns in unlabeled data
- Compare clustering algorithms for different data types
- Discover actionable insights using association rules

---

## Repository Structure

```
├── data/                  # Cleaned and raw datasets
├── clustering/
│   └── customersegmentation.ipynb    # bank customer credit worthiness identification
├── association_rule_mining/
│   └── arm.ipyb           # Support-confidence plots
└── README.md
```

---

## Methods and Results

### 1. Data Preprocessing
- Features used: `Age`, `Credit amount`, `Duration`
- Applied transformations to reduce skewness (log and box-cox)
- Scaled data using `StandardScaler`
- Imputed missing values in categorical features (`Saving accounts`, `Checking account`)

### 2. K-Means Clustering
- Applied on numerical features
- Evaluated using inertia and silhouette score
- Determined optimal `k` and interpreted clusters based on centroids

### 3. Hierarchical Clustering
- Linkage matrix computed using Ward’s method
- Visualized with dendrograms
- Cluster labels extracted using `AgglomerativeClustering`

### 4. K-Prototypes Clustering
- Used for clustering with numerical and categorical features
- Required categorical feature indices and used Huang’s distance
- Final clusters evaluated using cost function and interpretability

### 5. Association Rule Mining
- Applied on mall customer transactional data
- Frequent itemsets mined using Apriori algorithm
- Rules filtered and evaluated by:
  - Support: Frequency of the rule
  - Confidence: Probability of the consequent given the antecedent
  - Lift: Effectiveness of the rule over random chance
- Visualized support-confidence distribution and selected strong rules

---

## Key Learnings

- KMeans performs well on numerical data but is not suitable for mixed types
- Hierarchical clustering helps visualize structure but does not scale easily
- KPrototypes is practical for clustering real-world mixed datasets
- Association rules are effective in identifying product affinity and cross-selling opportunities

---

## Related Links

- Fellowship Progress Log : [Full Fellowship Progress](https://github.com/KushalRegmi61/AI_Fellowship_FuseMachines)



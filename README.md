# Clustering Countries Based on Life Quality Indicators:

## Project Overview:

This project applies clustering algorithms to analyze global countries based on various socio-economic features, aiming to identify natural groupings and investigate how Gulf Cooperation Council (GCC) countries compare to others.

Unsupervised learning techniques like **KMeans** and **Hierarchical Clustering** were applied to features such as:
- Income
- Education levels
- Fertility rate
- Urban population percentage
- Life expectancy
- Internet penetration

The project explores how countries form clusters when grouped solely based on data similarity, without predefined labels.

---

## 📊 Dataset Used:
[countries dataset in kaggle](https://www.kaggle.com/datasets/alirezaai/country-data)


---

## Techniques Used:

- **MinMaxScaler** for feature normalization  
- **PCA (Principal Component Analysis)** for dimensionality reduction and visualization  
- **KMeans** clustering  
- **Agglomerative Hierarchical Clustering** with different linkage methods (`ward`, `average`, etc.)  
- **Silhouette Score** and **Elbow Method** for model evaluation  
- **Matplotlib** and **Seaborn** for visual analysis

---

## Key Findings:

- PCA revealed strong linear patterns between variables, justifying dimensionality reduction to 2 components while preserving most of the variance.
- Clustering yielded **interpretable groups**, with GCC countries often appearing in similar clusters due to economic and demographic similarities.
- KMeans and Hierarchical Clustering produced **consistent groupings**, validated by Silhouette Scores.
- Feature correlation analysis helped eliminate redundancy (e.g., highly correlated variables like `income` and `life_expectancy`).

---

## What You’ll See in the Notebook:

- Clear, commented code and structured workflow
- Annotated scatter plots and dendrograms
- Country names displayed on cluster visualizations
- Comparison between raw and PCA-reduced data
- Analytical discussion on cluster membership (e.g., which countries are grouped with GCC countries and why)

---
## File Formats:

- Jupyter notebook file.
- PDF file.

---
## In-Depth Data Analysis & Insights:

To enrich the clustering results and understand the context of the countries (especially the GCC), we performed advanced exploratory data analysis (EDA) using visualizations and real-world reasoning.

---

### 1. Line Plot: Income vs. GDP

A line plot was used to show the relationship between individual income and GDP per capita. Country names were annotated for clarity.

**Insight:**
- A strong correlation was observed between income and GDP.
- GCC countries showed higher GDP values relative to income, suggesting strong oil-driven economies.

---

### 2. Histogram: Health Index for GCC Countries

We plotted a histogram for the `health` feature (representing overall citizen well-being) and marked the GCC countries with vertical lines.

**Insight:**
- The order of health scores in the dataset does not reflect current health rankings reported by the World Bank (2024).
- This discrepancy is likely due to outdated data. For example, Qatar and Saudi Arabia have seen rapid improvements due to events such as the 2022 FIFA World Cup and Vision 2030 projects.

**World Bank vs Dataset (Lowest to Highest Health Score):**
- Dataset: Qatar < Kuwait < Oman < UAE < Saudi Arabia < Bahrain  
- World Bank: Oman < Bahrain < Saudi Arabia < Kuwait < Qatar

*(Source: World Bank 2024 Health Index)*

---

### 3. Histogram: Imports and Exports

Side-by-side histograms were created to compare imports and exports across all countries, with vertical lines marking GCC countries.

**Insights:**
- **Imports:** UAE had the highest, possibly due to its strong tourism and luxury market. Qatar had the lowest.
- **Exports:** UAE also had the highest exports due to its diversified economy and trade hub status.
- **Note on Saudi Arabia:** Despite appearing to have low exports in the plot, Saudi Arabia is the largest actual exporter among GCC nations, mainly due to oil. However, its oil dependency causes fluctuations in export values.

**Interpretation:**
> High imports can indicate a dependency on foreign goods, which may signal economic imbalance. On the other hand, high exports often reflect economic strength and competitiveness.

---

These visual insights deepen the understanding of the data and help in interpreting the clustering results more effectively.


---
## ✅ Conclusions:

Clustering can be a powerful exploratory tool to uncover hidden structures in data, especially in international comparisons where labeled data may not exist. This project demonstrates how careful preprocessing, dimensionality reduction, and thoughtful interpretation can lead to insightful geopolitical and socio-economic analysis.




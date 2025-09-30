# Forecasting Election Outcomes in Contemporary Democracies  

## Project Overview  
This project investigates whether **machine learning models** can predict election outcomes more effectively than traditional opinion polls. Instead of forecasting which political party wins, the focus is on predicting whether the **incumbent government remains in power or is replaced**.  

The dataset spans **38 democracies (1900–2023)** and combines election outcomes with **social, political, and economic indicators** from trusted sources such as ParlGov, World Bank, OECD, UNESCO, and V-Dem.  

---

## Key Highlights  
- Built a **large multi-country dataset** of political, economic, and social indicators aligned with national election results.  
- Performed **data cleaning, imputation, and preprocessing** across dozens of indicators (GDP, inequality, democracy indices, conflict, urbanisation, etc.).  
- Applied **Principal Component Analysis (PCA)** to reduce redundancy and engineered composite indices (Political-Social Index, Economic Stability Index).  
- Used **hierarchical clustering** to group democracies with similar structures and developed **cluster-specific models**.  
- Benchmarked **Logistic Regression, Random Forest, and XGBoost** classifiers.  
- **Random Forest achieved the best accuracy (66% global, up to 82% in clusters)**, often **matching or surpassing polling accuracy**.  

---

## Repository Structure

Connor/, Eva/, Matt/, Yarkin/, Yeni/ethnic/, Zehn/

User-specific folders with intermediate cleaning outputs.

### 0.1 – 0.9 Notebooks (Data Cleaning)

0.1 Democratic & Economic – Data Cleaning → preprocesses democratic and economic indicators

0.2 Economic – Data Cleaning → focuses on core economic factors

0.3 Election Outcomes – Data Cleaning → prepares election results dataset

0.4 Ethnicity & Religion – Data Cleaning → processes demographic and religious data

0.5 Inflation – Data Cleaning → cleans inflation indicators

0.6 Multiple – Data Cleaning → handles multiple factor interactions

0.7 Politics – Data Cleaning → cleans political variables

0.8 Unemployment – Data Cleaning → processes unemployment rates

0.9 Urbanisation – Data Cleaning → processes urbanisation metrics


### 1 – 9 Main Analysis Notebooks

1 Data Combination → merges all cleaned datasets
2 Data Cleaning → final harmonisation and consistency checks
3 Exploratory Data Analysis → exploratory visualisations & correlations
4 Principal Component Analysis → dimensionality reduction using PCA
5 Election Averaging → aggregates election outcomes
6 Main Model → global ML models (Logistic Regression, Random Forest, XGBoost)
7 Clustering → hierarchical clustering of democracies into groups
8 Cluster Models → cluster-specific ML models
9 Polling Results → benchmarks models against polling data

### CSV Files

Final_Y_100325.csv → final cleaned dataset
fully-combined.csv → combined dataset after merging
Polling_Final.csv → polling data for benchmarking

### Other Files

Group_18_Final_Report.pdf → full written report
preprocess.py → preprocessing helper script
models.py → ML modelling helper script
evaluation.py → evaluation helper script
requirements.txt → Python dependencies
README.md → project documentation

---

## Dataset  
Data sources include:  
- **Election results**: ParlGov, Harvard Dataverse, national election commissions  
- **Democracy indicators**: V-Dem, IDEA Global State of Democracy Indices  
- **Economic indicators**: World Bank, OECD, World Inequality Database  
- **Social indicators**: UNDP Human Development Index, UNESCO, Transparency International  
- **Conflict data**: UCDP Armed Conflict Dataset  

---

## Results  
| Model                 | Accuracy (Full Dataset) | Accuracy (Cluster-Specific) |
|-----------------------|--------------------------|------------------------------|
| Logistic Regression   | ~52%                    | Up to 82% (Cluster 3)        |
| Random Forest         | ~66%                    | Up to 82%                    |
| XGBoost               | ~61%                    | 40–66%                       |

- Random Forest consistently outperformed other models.  
- Clustered models improved accuracy compared to global models.  
- ML approaches matched or outperformed polling in **over half of countries tested**.  

---

## Future Work  
- Expand dataset to include **coalition dynamics** and **local elections**.  
- Test **neural networks and ensemble meta-models**.  
- Integrate **psychological, technological, and historical features**.  
- Develop a reproducible **forecasting toolkit** for election observers and analysts.  

---

## Acknowledgements  
- Data from ParlGov, V-Dem, World Bank, OECD, UNESCO, Transparency International, UCDP.  
- Models built using **scikit-learn, pandas, numpy, matplotlib, seaborn, XGBoost**.  
- Project supervised by Jianqiao, University of Birmingham.  
```

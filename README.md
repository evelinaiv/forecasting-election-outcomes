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

election-forecasting/
├── notebooks/                         # Sequential workflow notebooks
│   ├── 0.1 - Democratic & Economic - Data Cleaning.ipynb
│   ├── 0.2 - Economic - Data Cleaning.ipynb
│   ├── 0.3 - Election Outcomes - Data Cleaning.ipynb
│   ├── 0.4 - Ethnicity & Religion - Data Cleaning.ipynb
│   ├── 0.5 - Inflation - Data Cleaning.ipynb
│   ├── 0.6 - Multiple - Data Cleaning.ipynb
│   ├── 0.7 - Politics - Data Cleaning.ipynb
│   ├── 0.8 - Unemployment - Data Cleaning.ipynb
│   ├── 0.9 - Urbanisation - Data Cleaning.ipynb
│   ├── 1 - Data Combination.ipynb          # Merges all cleaned datasets
│   ├── 2 - Data Cleaning.ipynb             # Final cleaning and harmonisation
│   ├── 3 - Exploratory Data Analysis.ipynb # EDA and feature exploration
│   ├── 4 - Principal Component Analysis.ipynb # PCA and dimensionality reduction
│   ├── 5 - Election Averaging.ipynb        # Aggregation of election outcomes
│   ├── 6 - Main Model.ipynb                # Global ML models (LogReg, RF, XGBoost)
│   ├── 7 - Clustering.ipynb                # Country clustering (hierarchical methods)
│   ├── 8 - Cluster Models.ipynb            # Cluster-specific ML models
│   └── 9 - Polling Results.ipynb           # Benchmarking vs. polling data
│
├── data/                              # Raw and processed data (not included in repo)
│   ├── Connor/                        # User-specific data cleaning outputs
│   ├── Eva/
│   ├── Matt/
│   ├── Yarkin/
│   ├── Yeni/
│   ├── Zehn/
│   ├── Final_Y_100325.csv             # Final cleaned dataset
│   ├── fully-combined.csv             # Combined dataset after merging
│   └── Polling_Final.csv              # Polling data for benchmarking
│
├── reports/
│   └── Group_18_Final_Report.pdf      # Full written report
│
├── src/                               # Helper scripts for reproducibility
│   ├── preprocess.py
│   ├── models.py
│   └── evaluation.py
│
├── requirements.txt                   # Python dependencies
└── README.md


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

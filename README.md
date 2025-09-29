# Teco-Customer-churn-analysis
This project focuses on performing an in-depth Exploratory Data Analysis (EDA) on a telecommunications customer dataset to understand the factors driving customer churn. Without building a predictive model, the goal is to uncover significant patterns, trends, and relationships between customer characteristics and their likelihood to cancel services


# Teco Customer Churn Analysis

**Author:** Pavan Kanade 

## Project overview
This repository contains an exploratory data analysis (EDA) of customer churn for Teco Telecom. The goal is to discover patterns and drivers of churn and provide actionable business recommendations to reduce customer attrition.

The dataset used contains **7,043** customers and a `Churn` target variable. Summary outcomes from the analysis include an overall churn of **~26.5%** and high-risk segments such as month-to-month contracts, fiber optic users, senior citizens, and customers with high monthly charges. (See the full report `Teco_Customer_Churn_Analysis Report.pdf` for details.)

---

## Repository structure
```
.
├─ data/
│  ├─ customer churn.csv            # original raw dataset
│  └─ processed/                    # (optional) preprocessed data
├─ notebooks/
│  └─ cutomer churn file.ipynb      # main EDA notebook (run top-to-bottom)
├─ reports/
│  └─ Teco_Customer_Churn_Analysis Report.pdf  # executive summary and findings
├─ assets/
│  └─ figures/                       # generated PNGs for README and slides
├─ requirements.txt                  # Python package list
├─ README.md                         # this file
└─ LICENSE
```

---

## How to run

1. Create an environment and install dependencies:
```bash
python -m venv venv
source venv/bin/activate      # Linux / macOS
venv\Scripts\activate         # Windows
pip install -r requirements.txt
```

2. Launch JupyterLab / Notebook and open the EDA notebook:
```bash
jupyter lab
# then open notebooks/cutomer churn file.ipynb and run all cells
```

3. (Optional) If `data/processed/processed.csv` exists, the notebook will load it directly. Otherwise the notebook performs preprocessing when run.

---

## Key findings (summary)
> Short summary pulled from the project report. For full details see `reports/Teco_Customer_Churn_Analysis Report.pdf`.

- **Overall churn:** ~**26.5%**  
- **Contract impact:** Month-to-month customers churn the most (~43.9%); two-year contracts churn extremely low (~2.7%).  
- **Internet service:** Fiber customers have higher churn (~44%) than DSL (~19.3%).  
- **Senior customers:** Higher churn (~41.9%).  
- **Billing:** Higher `MonthlyCharges` associates with higher churn; paperless billing users churn more than non-paperless users.

---

## Recommendations (business actions)
1. Target **month-to-month** and **fiber** customers with retention offers (discounts, free trials of add-ons).  
2. Incentivize longer contracts (1-year, 2-year) using bundled services and price breaks.  
3. Bundle **tech support** and **online security** add-ons for high-risk customers; these services correlate with lower churn.  
4. Analyze and personalize offers for **seniors** and **high monthly charge** segments.

---

## Notebook highlights
- `notebooks/cutomer churn file.ipynb` includes:
  - Data loading and summary statistics
  - Missing value handling and dtype fixes
  - Univariate and bivariate visualizations (distribution, bar charts, boxplots)
  - Churn-rate heatmaps and segmentation plots
  - Feature engineering (tenure groups, add-on counts)
  - (Optional) Baseline model with evaluation and feature importance

---

## Next steps / improvements
- Train and tune classification models, run SHAP or permutation importance to explain predictions.  
- Create a dashboard (Streamlit / Dash) for stakeholders to explore churn risk and offers.  
- Run A/B tests on recommended retention offers to measure impact.

---

## Contact
For questions or collaboration: pavankanade1110@gmail.com (7887844917)

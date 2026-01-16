
# Productivity Shocks and Sectoral Output Dynamics in India

## Project Overview
This project analyses how changes in productivity and macroeconomic conditions affect the performance of different industrial sectors in India over time. Using official macroeconomic, productivity, and industrial datasets, the analysis investigates how sectoral output responds before, during, and after productivity shocks, following the core intuition of DSGE (Dynamic Stochastic General Equilibrium) models.

The focus is on **interpretability, economic reasoning, and robustness**, rather than purely predictive accuracy.

---

## Key Research Questions
- Which industrial sectors are most sensitive to productivity changes?
- Which sectors are more resilient to economic shocks?
- Do productivity improvements benefit all sectors equally?
- What are the implications for business strategy, investment, and policy design in India?

---

## Data Sources
The analysis uses the following official datasets (annual frequency):

1. **Penn World Table (PWT 11.0)**  
   - GDP, employment, capital stock, productivity indicators  
   - Source: https://www.ggdc.net/pwt

2. **ILOSTAT Productivity Data**  
   - Output per worker  
   - Output per hour worked  
   - Source: https://ilostat.ilo.org/data/

3. **Index of Industrial Production (IIP), India**  
   - Sector-wise industrial output indices  
   - Source: Ministry of Statistics and Programme Implementation (MoSPI), India

All datasets are harmonised to a common time period and filtered for India.

---

## Methodology Overview
The analysis proceeds in five structured steps:

1. **Data Preprocessing**
   - Cleaning and aligning datasets by year
   - Constructing per-worker and per-hour macroeconomic variables
   - Computing growth rates to capture short-run dynamics

2. **Exploratory Data Analysis (EDA)**
   - Examining long-run productivity trends
   - Analysing sectoral output behaviour and volatility
   - Highlighting sectoral heterogeneity

3. **Shock Detection**
   - Decomposing aggregate productivity into trend and cycle (HP filter)
   - Identifying productivity shocks as large deviations from trend
   - Treating shocks as economy-wide disturbances

4. **Event Study Analysis**
   - Studying sectoral output dynamics before, during, and after shocks
   - Comparing responses across key industrial sectors
   - Emphasising dynamic adjustment patterns

5. **Regression Modelling**
   - Estimating simple, interpretable linear models
   - Benchmarking against naive and fixed-effects specifications
   - Using regressions as supporting evidence for event-study results

Causal claims are intentionally avoided due to data limitations.

---

## Repository Structure
```
project/
│
├── data/
│   ├── raw/              # Original datasets
│   └── processed/        # Cleaned and merged datasets
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_shock_detection.ipynb
│   ├── 04_event_study.ipynb
│   └── 05_modelling.ipynb
│
├── outputs/
│   ├── figures/          # Saved plots used in presentation
│   └── tables/           # Regression tables or summary outputs
│
├── README.md
└── requirements.txt
```

---

## Notebook Execution Order
Run the notebooks in the following order:

1. `01_data_preprocessing.ipynb`
2. `02_eda.ipynb`
3. `03_shock_detection.ipynb`
4. `04_event_study.ipynb`
5. `05_modelling.ipynb`

Each notebook saves outputs that are used by subsequent notebooks.

---

## Key Findings (Summary)
- Aggregate productivity exhibits a strong long-run upward trend with cyclical fluctuations.
- Sectoral output responses to productivity shocks are heterogeneous.
- Manufacturing and capital-intensive sectors are more sensitive to shocks.
- Utility-oriented sectors (e.g., electricity) display greater resilience.
- Productivity shocks have modest average effects, with gradual and dynamic adjustment.

---

## Limitations
- Annual data limits the detection of short-run dynamics.
- Shocks are statistically identified and not tied to specific historical events.
- Results are associative rather than causal.

---

## Tools and Libraries
- Python (pandas, numpy, matplotlib, statsmodels)
- Jupyter Notebooks

---

## Disclaimer
This project is intended for academic and analytical purposes. All interpretations are based on observed data patterns and should not be construed as causal policy recommendations.

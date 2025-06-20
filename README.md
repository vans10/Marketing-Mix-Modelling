# Marketing-Mix-Modelling
This is a Marketing Mix Modeling (MMM) project I completed during Spring 2025 at Babson College, where I analyzed two years of weekly data (2019–2020) for **Hope Street Cosmetics**, a luxury beauty brand. The objective was to evaluate marketing effectiveness, decompose sales drivers, and simulate ROI outcomes across channels using Python and Excel-based analysis.

---

## About the Brand

**Hope Street Cosmetics** is a premium skincare and cosmetics company, selling through:

-  Brand-Owned Stores  
-  Official Brand Website  
-  Specialty Retailers (e.g., Sephora, Ulta)  
-  Retailer.com  
-  Department Stores  

Despite a growing media budget, the brand experienced uneven growth, especially during COVID-19. This project aimed to identify ROI across marketing levers and suggest budget reallocations.

---

##  Project Scope

-  **Timeline:** Jan 2019 – Dec 2020 (weekly granularity)  
-  **Goal:** Build a modular, regression-based MMM to evaluate campaign ROI and sales impact  
-  **Deliverables:** Python-based model, Excel ROI simulation, and strategic recommendations

---

##  My Unique Contribution

I engineered a **custom seasonal dummy variable** to represent **International Women’s Day** campaigns. This allowed me to isolate uplift from March-based gender-focused brand activations — a relevant and data-aligned addition for a luxury beauty brand targeting female consumers.

---

##  Methodology

###  Data Treatment
- Cleaned and preprocessed weekly sales + media spend data using `pandas`  
- Applied **lag** and **adstock** transformations to capture delayed and decaying media effects  
- Created seasonal, event-based, and COVID-related dummy variables  
- Final modeling dataset: `final_database.csv`

###  Modeling
- Built an OLS regression model using `statsmodels`  
- Used a custom grid search (in `backend_v2.py`) to find optimal lag/adstock combinations  
- Evaluated model using R², t-stats, and coefficient interpretability  
- Separated baseline vs incremental sales contributions

###  ROI Analysis
- Exported model outputs to Excel  
- Created a scorecard to visualize ROI by channel and year  
- Conducted gap analysis and COVID-specific impact review

---

## Key Insights

- **Social Media** ROI increased from **15.7x** in 2019 to **17.1x** in 2020  
- **Search Marketing** maintained high efficiency with **10.2x** ROI  
- **Outdoor Advertising**, newly introduced in 2020, delivered a standout **44.2x** ROI  
- **TV and Print** saw diminishing returns, suggesting reallocation opportunities  
- COVID-related disruptions caused a $64M dip in expected sales  

---

##  ROI Scorecard (Sample)

| Channel         | 2019 ROI | 2020 ROI |
|----------------|----------|----------|
| Social Media    | 15.7     | 17.1  
| Search          | 8.1      | 10.2  
| TV              | 5.1      | 4.5  
| Print           | 3.0      | 2.7  
| Outdoor         | N/A      | 44.2  

---

##  Project Structure
HopeStreet_MMM/
│
├── data/
│ └── final_database.csv # Cleaned dataset
│
├── notebooks/
│ └── Modeling Workbook.ipynb # Full regression model in Python
│
├── scripts/
│ └── backend_v2.py # Custom adstock/lag modeling functions
│
├── analysis/
│ └── Final Excel.xlsx # ROI simulation tool
│
└── presentation/
└── Final_Presentation.pdf # Summary of findings


---

##  Tech Stack

- **Python (Jupyter Notebooks)**  
- **Pandas / NumPy / Statsmodels**  
- **Custom Regression Pipeline (`backend_v2.py`)**  
- **Excel for ROI analysis & simulations**  
- **PowerPoint for stakeholder storytelling**

---

##  Final Takeaways

This project helped uncover the true effectiveness of Hope Street’s marketing strategy. The insights were used to:

- Shift investment toward high-ROI digital channels  
- Recognize the lasting contribution of baseline/organic demand  
- Highlight the power of seasonal branding (e.g., Women’s Day campaigns)  
- Prepare a replicable MMM pipeline for future use

---

###  Author: Vanshika Gupta - www.linkedin.com/in/vanshikag10
*MS in Business Analytics, Babson College '25*  


# Global Financial Performance & Predictive Sales Analysis
***
> 💡 **Note on Dataset:** This project was developed during my internship period. It utilizes a real-time, real-world operational dataset provided directly by the host company to address actual business performance and forecasting challenges.
***
A comprehensive data analytics and machine learning project focused on evaluating global business operations (2013–2014). This project cleanses and analyzes a 700-record transactional dataset via Exploratory Data Analysis (EDA), builds a Multiple Linear Regression model to forecast sales volumes, and deploys an interactive Power BI dashboard for executive stakeholder reporting.

## 📌 Project Overview & Key Results

The business demonstrated strong commercial expansion during the analyzed period, scaling from a **$26.42M** revenue footprint in 2013 to **$92.31M** in 2014.

* **Total Sales:** $118.73M
* **Units Sold:** 1.13M units
* **Net Profit:** $16.89M
* **Overall Profit Margin:** 14.2%

---

## 🛠️ Tools & Technologies Used

* **Programming Language:** Python
* **Data Manipulation & Preprocessing:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Data Visualization:** Matplotlib, Seaborn
* **Business Intelligence & Dashboards:** Power BI Desktop

---

## ⚙️ Methodology & Implementation

### Phase 1: Exploratory Data Analysis (EDA)
* **Data Integrity:** Handled data hygiene by stripping trailing whitespace from columns and addressing null values isolated within the `Discount Band` column.
* **Distribution Check:** Univariate analysis revealed that both *Sales* and *Profit* metrics are heavily right-skewed—a classic characteristic of B2B structures where frequent low-value transactions are balanced by high-value contract closures.
* **Feature Relationships:** Bivariate analysis identified a near-perfect mathematical correlation ($r \approx 1.0$) between `Sales`, `Gross Sales`, and `COGS`.

### Phase 2: Predictive Modelling (Regression)
To engineer a realistic predictive framework, variables containing post-transaction financial summaries (`Gross Sales`, `COGS`, `Profit`) were excluded to prevent **data leakage** and perfect **multicollinearity**.
* **Target Variable:** `Sales`
* **Features:** `Units Sold`, `Sale Price`, `Segment`, and `Country`
* **Preprocessing:** Categorical variables were transformed using One-Hot Encoding (`pd.get_dummies()`).
* **Modeling:** Built using an 80/20 train-test split utilizing the `LinearRegression` module from Scikit-Learn.

### Phase 3: Business Intelligence (Power BI Dashboard)
An interactive executive dashboard was constructed using a strategic information hierarchy:
* **High-Level KPI Blocks:** Total Sales, Profit, and Volume pinned to the top header for instant visibility.
* **Temporal Trends:** A dual-line timeline chart capturing revenue trajectory variations across months.
* **Categorical & Regional Share:** A donut chart illustrating product performance share paired with vertical bar charts tracking sales by country.
* **Interactive Layer:** Dynamic slicers filtering data instantly by *Segment* and *Year*.

---

## 📈 Core Insights & Financial Performance

### Market Segment Analysis
* **Government (The Core Driver):** Generates **$52.50M (44.2%)** of total revenue. It stands as a highly optimized segment with a strong **21.7%** net profit margin.
* **Channel Partners (The Hidden Asset):** Represents a small portion of gross sales ($1.80M) but operates at an extraordinary **73.1%** profit margin, yielding **$1.32M** in pure profit due to low-overhead parameters.
* **Enterprise (The Financial Risk Area):** Contributed a substantial **$19.61M** in top-line volume but generated a net loss of **-$614,545 (-3.1% margin)**.

### Product & Regional Standouts
* **Flagship Product:** `Paseo` is the enterprise's clear leading product line, driving **$33.01M** in gross sales volume.
* **Geographic Distribution:** Revenue is exceptionally well-balanced internationally:
  * **United States:** $25.03M *(Highest volume)*
  * **Canada:** $24.89M
  * **France:** $24.35M
  * **Germany:** $23.51M

---

## 🚀 Strategic Recommendations

1. **Fix the Enterprise Profit Drain:** Immediately audit the price structures, cost of goods sold (COGS), or aggressive discount bands applied to the *Enterprise* segment to halt capital erosion.
2. **Optimize U.S. Pricing Schemes:** The U.S. generates the highest top-line sales volume ($25.03M) but holds the lowest national profit margin (**11.9%**). Adopting the pricing and distribution models used in France and Germany (which yield **>15.5%** margins) is highly recommended.
3. **Scale the Channel Partner Model:** Because Channel Partners boast a **73.1%** margin profile, even modest increases in marketing and distribution allocations to this channel will directly boost bottom-line net profit.

---
## 👥 Prepared By
* **Name:** Priyanshu Vijay
  
## ⚖️ License & Attribution

This project is open-source software licensed under the **MIT License**.
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](/LICENSE)


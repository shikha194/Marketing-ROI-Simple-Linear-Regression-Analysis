# Marketing ROI: Simple Linear Regression Analysis

## 📌 Project Overview
This repository contains a data analytics project that models the relationship between marketing campaign budgets and revenue. Working as part of an analytics team, the primary objective is to investigate the directional impact and magnitude of different Promotion methods on cross-company **Sales** revenue. 

Using an exploratory data analysis (EDA) and ordinary least squares (OLS) regression framework, this project provides data-driven insights to help company executives strategically allocate future marketing resources across TV, radio, and social media.

---

## 📉 Core Objective & Modeling Framework

* **Business Problem:** Determine if increasing investment in any of the advertising methods yields a statistically significant increase in sales, and quantify that return.
* **Dependent Variable ($Y$):** `Sales` (expressed in millions of dollars)
* **Independent Variable ($X$):** `Radio Budget` (expressed in millions of dollars) - The one variable that has linear relationship with Sales

### 📐 Regression Assumptions Evaluated
Before finalizing predictions, the model verifies the core OLS linear regression assumptions:
1. **Linearity:** Linear relationship between the independent and dependent variables (assessed via scatter plot).
2. **Independence:** Observations are independent of one another.
3. **Homoscedasticity:** Residuals maintain constant variance across all levels of the independent variable.
4. **Normality:** Residuals are normally distributed (assessed via histogram and Q-Q plot).

---

## 🛠️ Tech Stack & Libraries
* **Python 3**
* **Pandas:** Data loading, inspection, and missing value cleanup.
* **Matplotlib & Seaborn:** Exploratory scatter plots, residual distribution plotting, and trend line visualization.
* **Statsmodels:** Fitting the OLS simple linear regression model and extracting detailed summary coefficients.

---

## 📊 Methodology & Analytical Steps

### 1. Data Cleaning & Exploration
The initial fictional dataset (`marketing_sales_data.csv`) contains 572 rows detailing promotional information. Missing rows were isolated and handled using `.isna()` structures to ensure data consistency. Descriptive analytics and scatter plots were used during EDA to verify a strong, positive monotone relationship between radio spending and revenue.

### 2. Model Estimation (OLS)
The regression model was constructed using the formula interface:
```python
from statsmodels.formula.api import ols
import statsmodels.api as sm

OLS_model = ols(formula=model_formula, data=data)

```

# Project Insights: Key Findings & Strategic Recommendations

## 📈 Key Findings & Statistical Results

The Ordinary Least Squares (OLS) regression model yielded definitive metrics regarding the impact of radio advertising on commercial revenue:

* **Statistical Significance:** The relationship between the radio promotion budget and sales is highly statistically significant, underscored by an exceptional p-value of **0.000**.
* **Model Precision:** The model demonstrated low variance in its parameter estimations, yielding a remarkably tight Standard Error of **0.194**.
* **Y-Intercept ($\beta_0$):** `41.5326`
* **Slope/Radio Coefficient ($\beta_1$):** `8.1733`

### 📝 Mathematical Equation
$$\text{Sales (in Millions)} = 41.5326 + 8.1733 \times \text{Radio Budget (in Millions)}$$

### 💡 Interpretation of Coefficients
* **Baseline Sales ($\beta_0$):** For companies with a radio promotion budget of \$0, the baseline average sales are estimated at **\$41.533 million**.
* **Marginal Return ($\beta_1$):** For every \$1 million increase in the radio promotion budget, sales revenue is expected to increase by an average of **\$8.173 million**.

---

## 🎯 Strategic Business Recommendations

Based on the statistical strength of the OLS model, the following insights are presented to stakeholders and company leadership to guide future marketing resource allocation:

1. **Continue and Expand Radio Promotions:** Because the relationship is notable and mathematically validated ($p = 0.000$), it is highly recommended to continue using radio influencer promotions to market products and services.
2. **Targeted Budget Decisions:** If company leaders seek to grow revenue by approximately \$8.17 million, they can confidently propose a \$1 million budget expansion dedicated specifically to the radio promotion budget.
3. **Data-Driven Resource Optimization:** Executive teams should utilize the derived linear formula to forecast returns and justify marketing spend shifting from unverified channels into highly predictable, high-return radio campaigns.


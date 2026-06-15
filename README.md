# Statistical Analysis of Birth Weight and Customer Churn

### Business Statistics

## Project Overview
This project applies statistical analysis and regression modelling to two real-world datasets. The analysis covers key statistical concepts including descriptive statistics, linear regression, logistic regression, and assumption testing, with the goal of identifying factors that influence birth weight and customer churn.

## Datasets
- **Birthweight.csv** — 1,388 birth records with variables including birth weight, family income, cigarettes smoked during pregnancy, and gender
- **CustomerChurn.CSV** — Customer dataset with variables including Monthly Charges, Viewing Hours Per Week, and Churn status

## Tools & Technologies
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Statsmodels, SciPy
- **Environment:** Jupyter Notebook

## Analysis Structure

### Section 1 — Statistical Concepts
- Discussion of the distinction between **parameters** (population-level) and **statistics** (sample-level estimates)

### Section 2 — Linear Regression (Birthweight Dataset)
**Dependent Variable:** Birth weight (lbs)

**Independent Variables:**
- Family Income (continuous)
- Cigarettes smoked per day during pregnancy (continuous)
- Gender / Male (categorical)

**Key Results:**
| Variable | Coefficient | P-Value | Interpretation |
|---|---|---|---|
| Family Income | +0.0061 | 0.001 | Higher income → slightly higher birth weight |
| Cigarettes per day | -0.0288 | 0.000 | More smoking → lower birth weight |
| Male | +0.1946 | 0.004 | Male babies tend to weigh more |

- **R² = 0.036** — model explains 3.6% of variance in birth weight
- Overall model statistically significant (F-statistic p-value < 0.001)

**Assumption Checks Performed:**
- Linearity — Residuals vs Fitted values plot
- Independence — Durbin-Watson statistic (1.927, no autocorrelation)
- Homoscedasticity — Breusch-Pagan test (p = 0.976, confirmed)
- Normality — Q-Q plot and Shapiro-Wilk test (residuals not normally distributed)
- Multicollinearity — VIF values all below 10 (no multicollinearity detected)

### Section 3 — Logistic Regression (Customer Churn Dataset)
**Dependent Variable:** Churn (1 = churned, 0 = retained)

**Independent Variables:**
- Monthly Charges
- Viewing Hours Per Week

**Key Results:**
| Variable | Coefficient | P-Value | Interpretation |
|---|---|---|---|
| Monthly Charges | +0.0618 | 0.000 | Higher charges → higher churn probability |
| Viewing Hours Per Week | -0.0305 | 0.000 | More viewing → lower churn probability |

- **Pseudo R² = 0.0285** — model explains ~2.85% of variance in churn
- Likelihood ratio test significant (p < 0.001), model outperforms null model

### Section 4 — Reflection
- Key learning points from the analysis
- Challenges encountered (missing values, non-normal residuals, low R²) and strategies to address them

## Key Findings
- Smoking during pregnancy has a statistically significant negative effect on birth weight
- Higher family income is associated with slightly higher birth weight
- Male babies tend to have higher birth weight than female babies
- Customers with higher monthly charges are more likely to churn
- Customers who watch more hours per week are less likely to churn

## Files
| File | Description |
|---|---|
| `business_statistics_report.ipynb` | Full Jupyter Notebook with code, outputs, and commentary |
| `Birthweight.csv` | Birth weight dataset used in linear regression analysis |
| `CustomerChurn.CSV` | Not included — university-provided dataset, available on request |

## Author
**Zakaria Gou-Ali**
MSc Business Analytics — University of Greenwich
[LinkedIn](https://www.linkedin.com/in/zakaria-gou-ali-896175347/)

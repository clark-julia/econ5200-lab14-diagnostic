# econ5200-lab14-diagnostic
# OLS Diagnostics: Robust and Clustered Standard Errors

## Objective
I examined how heteroskedasticity, within-firm correlation, and influential observations affect OLS estimates and standard errors.

## Methodology
- Simulated data with heteroskedastic errors and measured how often nominal 95% confidence intervals captured the true slope.
- Compared classical, HC1, and HC3 standard errors.
- Simulated data with errors shared within 40 firms and compared HC3 standard errors with firm-clustered standard errors.
- Calculated leverage, studentised residuals, and Cook's distance to identify influential observations.
- Compared regression slopes with and without the three planted observations.
- Used AI to write a Python function that calculates six types of standard errors and checked its results against statsmodels.

## Key Findings
- With heteroskedastic errors, classical standard errors achieved 92.4% coverage, compared with 94.4% for HC3.
- With errors correlated within firms, HC3 coverage dropped to 50.3%, while clustering by firm restored coverage to 93.7%.
- One planted observation significantly changed the slope from 1.4927 to 1.4468.
- The AI-generated function passed all 18 standard error comparisons against statsmodels in the first round. All 18 values also matched when the column names were changed.

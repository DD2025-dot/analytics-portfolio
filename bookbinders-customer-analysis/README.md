# Bookbinders: Customer Analysis & Statistical Testing

**Question:** What do a book club's customers buy, and can purchases tell us who they are?

## Approach
- Confidence intervals, t-tests and chi-square tests on customer data
- Linear and logistic regression, variable importance, partial dependence plots
- Predicted customer gender from purchase categories

## Key insights
- Spend on books and non-books is **weakly related** (correlation 0.157, 95% CI 0.149 to 0.166)
- Men make **more purchases per customer** than women: 4.9 vs 3.4 (p < 0.001)
- State and purchase of one title are **borderline related** (chi-square p = 0.052)
- **DIY books** are the strongest gender signal: dropping them costs ~11% of model performance
- Spend history and recency are **not** useful for predicting gender
- Plots and distributions explain *why*: spend overlaps heavily across groups, DIY purchases do not

## Files
- [Report (HTML)](bookbinders_analysis.html)
- [Source (Rmd)](bookbinders_analysis.Rmd)

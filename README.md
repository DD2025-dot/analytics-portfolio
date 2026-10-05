# Analytics & Strategy Portfolio

**Deepa Das** | Operations Manager, Amazon (Kansas City) | MBA '25 | 10 years in program management

Six projects that turn customer data into **who to target, what to offer, and what it is worth**. Every project ends in a dollar figure and a recommendation.

## Projects

| # | Project | Business question | Headline result |
|---|---|---|---|
| 1 | [Creative Gaming: Uplift Model](creative-gaming-uplift/) | Which players does an ad actually *persuade*? | Uplift targeting earned **$55.7K vs $21.9K** for propensity targeting |
| 2 | [Creative Gaming: Propensity Model](creative-gaming-propensity/) | Can a model pick the best 30K players for ads? | Random forest lifted profit to **$96K**, up from $13.7K for random ads |
| 3 | [Tuango: Push Messages](tuango-push-targeting/) | Who should get a mobile deal message? | Blanket send loses **3.2M RMB**; targeting turns it profitable |
| 4 | [Intuit QuickBooks: Direct Mail](intuit-quickbooks-targeting/) | Which 25K customers get the cloud offer? | Neural net beat logistic (**AUC 0.83 vs 0.76**), ~$131K expected profit |
| 5 | [S-Mobile: Churn](smobile-churn-prediction/) | Which retention offers pay off? | Only the **network fix** is profitable; device upgrades lose money at $50 |
| 6 | [Bookbinders: Customer Analysis](bookbinders-customer-analysis/) | What drives customer behavior and gender mix? | **DIY books** are the strongest gender signal |

## Skills shown
- **Customer analytics:** targeting, segmentation, churn, uplift, propensity
- **Modeling:** logistic regression, random forests, neural networks
- **Evaluation:** gains curves, AUC, Qini curves, train/test discipline
- **Business framing:** break-even rules, incremental profit, ROI of offers
- **Statistics:** confidence intervals, t-tests, chi-square, regression

## How to use this repo
- Each project folder has a **README** (summary) and an **.html report** (full code and output)
- `data/` holds the datasets the notebooks load
- Language: **R** (R Markdown)

## Run it yourself
- Install: `tidyverse`, `ranger`, `caret`, `nnet`, `vip`, `pdp`, `yardstick`, `janitor`, `skimr`, `statar`, `splitstackshape`
- Helper package for gains / Qini / importance plots: `remotes::install_github("blakemcshane/kelloggmktg482")`
- Open any `.Rmd` and click **Knit**. Data loads from `../data/`

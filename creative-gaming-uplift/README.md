# Creative Gaming: Uplift Modeling to Optimize Ad Targeting

**Business question:** Which customers should we target with an in-app ad, so that we pay only for customers the ad actually *persuades* rather than customers who would have converted anyway?

**Context:** Kellogg MBA, Customer Analytics & AI (MKTG 482). A randomized ad experiment on a mobile game's user base: 150,000 users, 19 behavioral features. The target is conversion (purchase). Profit per conversion is $14.99 and an ad costs $1.50 per targeted user.

## Approach
1. Built a stacked dataset from the randomized control and treatment groups, then did a stratified 70/30 train/test split.
2. Trained two random forests (`ranger`), one on treated users and one on control users. The **uplift score** is the difference between predicted conversion with and without the ad.
3. Evaluated both uplift and propensity targeting with Qini curves and uplift bar plots across 20 groups.
4. Converted model performance to **incremental profit**, and found the profit-maximizing share of customers to target (break-even rule: expected incremental conversion value > ad cost).

## Results (scaled to a 120,000-user campaign)
| Model | Optimal % targeted | Incremental profit |
|---|---|---|
| Propensity (who is likely to buy) | 50% | ~$21.9K |
| **Uplift (who is persuaded by the ad)** | **30%** | **~$55.7K** |

Uplift targeting earned roughly **$33.9K more** while reaching fewer customers. A propensity model spends budget on "sure things" who convert without an ad, while an uplift model isolates the persuadable segment.

## Files
- [`creative_gaming_uplift.html`](creative_gaming_uplift.html): full rendered report with code, output and interpretation
- [`creative_gaming_uplift.Rmd`](creative_gaming_uplift.Rmd): R Markdown source

**Tools:** R, ranger (random forests), tidyverse, caret, Qini/uplift evaluation.

*The dataset is Kellogg course material and is not included, so the notebook will not run without it. The rendered HTML contains all outputs.*

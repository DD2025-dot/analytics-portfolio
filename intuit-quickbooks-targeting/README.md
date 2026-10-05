# Intuit QuickBooks Online: Direct Mail Targeting

**Question:** From 25,000 customers on the wave-2 list, who should get the cloud-upgrade mailing?

## Setup
- Net benefit per responder **$180**, mailing cost **$1.60**
- Wave 1 (50,000 customers) provides training data
- Rule: mail only if expected profit after cost is at least **$5.60** (the opportunity cost)

## Approach
- Logistic regression vs neural network, trained on wave 1
- Compared with gains curves and AUC on held-out data
- Scored wave 2, then picked customers above the profit hurdle

## Key insights
| Model | Test AUC | Customers mailed | Expected profit |
|---|---|---|---|
| Logistic regression | 0.755 | 8,118 | $125.6K |
| Neural network | 0.833 | 8,201 | **$131.4K** |

- **Neural net wins:** better ranking and about $5.8K more expected profit
- Mailing only ~1 in 3 customers beats mailing everyone
- Break-even response rate is **0.89%** (1.60 / 180)
- With **no** opportunity cost, you would mail ~13-15K customers, but profit per customer falls to ~$10-11

## Files
- [Main analysis (HTML)](intuit_targeting.html) | [Rmd](intuit_targeting.Rmd)
- [Break-even sensitivity (HTML)](intuit_breakeven_analysis.html) | [Rmd](intuit_breakeven_analysis.Rmd)

# Creative Gaming: Propensity Model

**Question:** Can a model pick the best 30,000 of 150,000 players to show an ad, and by how much does it beat random targeting?

## Setup
- Profit per conversion **$14.99**, ad cost **$1.50** per user
- Three groups of 30K players: no ad, random ad, model-selected ad

## Approach
- Logistic regression on organic (no-ad) behavior, then retrained on ad-exposed users
- Random forest on ad-exposed users
- Compared with gains curves, AUC and profit on a held-out scoring sample

## Key insights
| Group | Conversion | Profit |
|---|---|---|
| No ad (control) | 5.7% | $25.6K |
| Random ads | 13.0% | $13.7K |
| Model-selected top 30K | 21.5% | **$51.7K** |

- **Ads alone lose money:** conversion more than doubles, but ad cost eats the gain
- **Targeting fixes it:** the model doubles profit versus no ad
- **Model trained on the wrong behavior fails:** AUC drops from 0.80 (organic) to 0.64 on ad-exposed players
- **Retrain on ad data:** AUC 0.70, profit **$78.2K** (+$26.5K)
- **Random forest:** AUC 0.79, profit **$96.4K** (+$18.3K more)
- Once ads exist, **ad clicks** matter more than past in-game activity

## Files
- [Report (HTML)](propensity_model.html)
- [Source (Rmd)](propensity_model.Rmd)

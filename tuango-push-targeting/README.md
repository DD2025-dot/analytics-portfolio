# Tuango: Targeting Mobile Push Messages

**Question:** A Karaoke deal can go to ~397K app users. Should we message everyone, or only likely buyers?

## Setup
- Deal price **49 RMB**, Tuango keeps **50%** (24.5 RMB)
- Cost of each push message **11 RMB**
- Break-even response rate = 11 / 24.5 = **44.9%**

## Approach
- Logistic regression and neural network predicting purchase
- Decile analysis of predicted vs actual response
- Profit simulation: message everyone vs only customers above break-even

## Key insights
- Average response rate is only **12%**, far below the 44.9% break-even
- **Messaging everyone loses about 3.2M RMB**
- Model separates buyers well: top decile responds **28%**, bottom decile **2.4%** (11x gap)
- Biggest purchase drivers: **messages on**, past spend, deal frequency, being female, younger age
- Targeting only above-break-even customers turns the campaign **profitable**
  - Logistic: ~0.4% of customers, +7.2K RMB
  - Neural network: ~0.9% of customers, +11.3K RMB
- Order size could **not** be predicted from the available variables

## Files
- [Report (HTML)](tuango_targeting.html)
- [Source (Rmd)](tuango_targeting.Rmd)

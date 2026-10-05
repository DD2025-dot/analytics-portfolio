# Creative Gaming: Uplift Model

**Question:** Which players should see an in-app ad, so we pay only for players the ad actually *persuades*?

## Setup
- 150K users, 19 behavior features, randomized ad experiment
- Profit per conversion **$14.99**, ad cost **$1.50** per user
- Goal: maximize **incremental** profit (versus showing no ad)

## Approach
- Stacked control and treated groups, stratified 70/30 train/test split
- Trained two random forests (`ranger`): one on ad-exposed users, one on control users
- **Uplift score** = P(convert with ad) - P(convert without ad)
- Compared against a propensity model using Qini curves (20 groups)

## Key insights
- **Uplift beats propensity:** about **$55.7K** vs **$21.9K** incremental profit
- **Target less, earn more:** uplift's best cutoff is **30%** of users; propensity's is **50%**
- Propensity models spend budget on "sure things" who would buy anyway
- Uplift isolates the **persuadable** customers
- Past ~90% of users targeted, the ad *destroys* value (negative uplift)

## Files
- [Report (HTML)](uplift_model.html)
- [Source (Rmd)](uplift_model.Rmd)

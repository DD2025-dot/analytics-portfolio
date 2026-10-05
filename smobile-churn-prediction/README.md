# S-Mobile: Churn Prediction & Retention Offers

**Question:** Why do customers leave, and which retention offer is worth paying for?

## Approach
- Logistic regression predicting churn
- Ranked drivers by coefficient size and significance
- Designed 3 offers tied to the drivers and simulated their effect on predicted churn
- Assumptions: **$100** revenue per customer per month, **18-month** retention window

## Key insights
- **Top churn drivers:** blocked voice calls, device age, number of subscribers on the account, usage, credit rating
- Customers with strong credit and higher usage are **more loyal**

| Offer | Customers | Churn before | Churn after | Net profit |
|---|---|---|---|---|
| Network fix ($10) | 742 | 6.2% | 5.2% | **+$5.9K** |
| Device upgrade ($50) | 1,500 | 6.6% | 5.0% | -$31.7K |
| Bonus minutes ($5) | 136 | 5.6% | 5.5% | -$0.6K |

- **Network fix is the only profitable offer** and has the best return per dollar
- **Device upgrades work but cost too much:** break-even is about **$29** per handset
- **Bonus minutes barely move churn:** drop the offer

## Files
- [Report (HTML)](churn_prediction.html)
- [Source (Rmd)](churn_prediction.Rmd)

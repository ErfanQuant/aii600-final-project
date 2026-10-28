# Decisions

This file is the history of the project. Append an entry when a choice changes the work: the quantity, the data, the split, the model, the loss, or the action. Leave old entries in place. A later entry can reverse an earlier one. If a result depends on a random draw, record the seed under Why. The split entry records the cutoff date, or the seed and the fraction. The pull request that merges the code names this entry.

## YYYY-MM-DD: short title

- Decision. I chose to investigate Bayesian machine learning for risk-aware portfolio allocation. I will use Bayesian Student-t regression to forecast the distribution of weekly US equity market excess returns and evaluate whether it improves portfolio growth while controlling downside risk.
- Why. My goal is to connect probability, Bayesian estimation, uncertainty, and financial decision-making in a practical research problem. Student-t regression allows for heavy-tailed returns, while Bayesian estimation accounts for parameter uncertainty. I will compare it with frequentist Student-t regression to evaluate whether the Bayesian approach provides additional value. This direction also supports my interest in quantitative finance.
- Alternative. I initially considered Bayesian logistic regression to predict the probability of a large weekly market decline. I decided not to use it because a binary outcome does not distinguish between moderate and severe losses once both exceed the selected threshold. Modeling continuous returns provides more information about the magnitude of potential losses, which is important for portfolio allocation.
- Revisit. I will reconsider this approach if the Bayesian model produces poorly calibrated predictions, fails to improve the out-of-sample portfolio growth–downside-risk tradeoff, or performs inconsistently under different market conditions and investor risk preferences.

# Proposal


## Hypothesis
I want to investigate whether Bayesian machine learning can improve portfolio growth while controlling downside risk. My hypothesis is that Bayesian Student-t regression, which accounts for parameter uncertainty and allows for heavy-tailed returns, can produce better investment decisions than frequentist Student-t regression and fixed investment strategies.
The quantity I will forecast is the probability distribution of US equity market excess returns over the following trading week, measured in percentage points.

## Data
I plan to use weekly US equity market excess returns and risk-free returns from the Kenneth French Data Library, together with VIX observations from FRED. Each observation represents one trading week, with predictors based on information available before the following week's return. The study period will be approximately 1990–2026, subject to data availability.
These measurements differ from actual investment outcomes: research-based market returns may differ from tradable ETF returns, while VIX measures approximately 30-day implied volatility rather than one-week losses. These differences can introduce systematic bias that more observations may not remove. 
As a possible extension, I may use NLP to extract sentiment or uncertainty indicators from public financial announcements.

## Decision affected by the model
A risk-averse portfolio manager allocates a hypothetical $100,000 portfolio between US equities and short-term Treasury securities each week. The decision balances expected returns against downside risk, measured by Conditional Value at Risk (CVaR), while accounting for transaction costs.
Missing a severe market decline may cause substantial losses, while unnecessarily reducing equity exposure sacrifices potential growth. The relative cost of these outcomes depends on investor risk preferences, which I will examine through sensitivity analysis.
I will compare Bayesian and frequentist Student-t regression using the same allocation rule, alongside buy-and-hold equities and a fixed 60/40 portfolio.
Evaluation will include walk-forward out-of-sample testing, predictive calibration, realized portfolio growth, downside risk, and trading costs.



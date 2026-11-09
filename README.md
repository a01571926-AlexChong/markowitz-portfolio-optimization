# Portfolio Optimization Using Modern Portfolio Theory

### Markowitz Optimization | Risk Analysis | Rolling-Window Backtesting | Excel

## Project Overview

As part of my preparation for the CFA Level I exam, I developed this project to apply concepts from Quantitative Methods and Portfolio Management to real financial market data.

The main objective was to evaluate whether portfolios constructed using Markowitz's Modern Portfolio Theory could outperform a simpler Equal-Weighted strategy in terms of returns and risk-adjusted performance.

Rather than relying only on historical optimization, I tested how the strategies performed on unseen data, examined the impact of monthly reoptimization, and considered transaction costs.

The entire analysis was developed in Microsoft Excel.

## 1. Dataset

The analysis covers **60 monthly return observations** for five publicly traded companies:

| Ticker | Company |
|---|---|
| AAPL | Apple Inc. |
| JPM | JPMorgan Chase & Co. |
| JNJ | Johnson & Johnson |
| XOM | Exxon Mobil Corporation |
| WMT | Walmart Inc. |

The dataset was divided into:

- **Training period:** 48 months for estimating expected returns and the covariance matrix.
- **Testing period:** 12 months for out-of-sample performance evaluation.
- **Benchmark:** SPDR S&P 500 ETF Trust (SPY).
- **Risk-free rate assumption:** 4% annually.

## 2. Portfolio Construction

Three investment strategies were evaluated:

**Equal-Weighted Portfolio**

Allocates 20% to each stock. This serves as a simple diversification benchmark that does not depend on estimated optimal portfolio weights.

**Minimum Variance Portfolio**

Uses Markowitz optimization to identify the combination of assets that minimizes expected portfolio volatility.

**Maximum Sharpe Portfolio**

Identifies the portfolio with the highest estimated excess return per unit of risk.

The optimization was performed using Excel Solver, subject to the following constraints:

- Portfolio weights sum to 100%.
- Short selling is not allowed.
- Individual asset weights range from 0% to 100%.

## 3. Methodology

The project includes the following analyses:

### Efficient Frontier and Capital Allocation Line

Constructed the Efficient Frontier to evaluate the relationship between expected portfolio returns and volatility across different asset allocations.

The Capital Allocation Line was used to illustrate the risk-return combinations available when combining a risky portfolio with a risk-free asset.

### Portfolio Risk Analysis

Evaluated the strategies using:

- Annualized volatility
- Sharpe Ratio
- Value at Risk (VaR)
- Conditional Value at Risk (CVaR)
- Maximum Drawdown
- Correlation and covariance matrices

### Out-of-Sample Backtesting

Portfolio weights were estimated using the first 48 months of historical returns and evaluated over the following 12 months.

This allowed me to compare historical optimization results against realized investment performance.

### Rolling-Window Backtesting

Implemented a 48-month rolling estimation window with monthly reoptimization.

At each step, portfolio weights were recalculated using the previous 48 months of data and then applied to the following month's returns.

This approach evaluates whether regularly updating portfolio allocations improves performance compared with maintaining the original optimized weights.

### Sensitivity Analysis

Tested the Maximum Sharpe strategy under three annual risk-free rate assumptions: 2%, 4%, and 6%.

The objective was to examine how changes in the risk-free rate affected the optimized portfolio weights and expected risk-adjusted performance.

### Transaction Costs

Included an assumed transaction cost of 0.10% of traded value to estimate the effect of portfolio turnover on net returns.

## 4. Key Findings

The 12-month out-of-sample backtest produced the following results:

| Strategy | Return |
|---|---:|
| Equal-Weighted | 32.27% |
| Static Minimum Variance | 35.70% |
| Static Maximum Sharpe | 29.40% |
| Rolling Minimum Variance | 37.20% |
| Rolling Maximum Sharpe | 20.19% |

**Equal-Weighted delivered the strongest risk-adjusted performance.**

Despite its simple allocation approach, Equal-Weighted achieved a 32.27% return, 9.52% annualized volatility, and a Sharpe Ratio of approximately 2.60.

**Rolling Minimum Variance achieved the highest absolute return.**

The strategy generated a 37.20% gross return, declining to 36.89% after estimated transaction costs.

**Rolling Maximum Sharpe underperformed the other strategies.**

Its weaker out-of-sample results suggest that maximizing historical risk-adjusted returns does not necessarily lead to superior future performance.

The results highlight the importance of estimation risk, diversification, and testing portfolio strategies outside the period used for optimization.

## 5. Investment Conclusion

Based on the observed results, the Equal-Weighted Portfolio offered the strongest balance between risk and return during the testing period.

Although Rolling Minimum Variance achieved a higher absolute return, Equal-Weighted experienced lower realized volatility and a smaller maximum drawdown.

The findings suggest that more complex portfolio optimization does not always translate into better investment performance, particularly when historical estimates fail to reflect future market conditions.

## 6. Limitations

Several limitations should be considered when interpreting the results:

- The analysis includes only five stocks.
- The out-of-sample testing period covers 12 months.
- Historical estimates may not accurately represent future market conditions.
- Transaction costs are modeled assumptions and may differ from actual execution costs.
- Monthly reoptimization may produce unstable allocations.
- The benchmark comparison requires consistent adjusted-price data and matching observation dates.

The results are historical and should not be interpreted as forecasts or guarantees of future performance.

## 7. Project Files

**Excel Model:** `Markowitz_Portfolio_Optimization.xlsx`

Contains historical returns, covariance matrices, portfolio optimization, Efficient Frontier, risk analysis, backtesting, sensitivity analysis, and investment recommendations.

**Financial Research Report:** `Portfolio_Optimization_Research_Report.pdf`

Presents the research objective, methodology, main results, interpretation, and final conclusions.

## 8. Tools and Skills Applied

- Microsoft Excel
- Excel Solver
- Portfolio Optimization
- Modern Portfolio Theory
- Quantitative Financial Analysis
- Risk Management
- Out-of-Sample Backtesting
- Investment Performance Evaluation

---

*This project was developed for educational and research purposes as part of my independent CFA Level I preparation. It does not constitute personalized investment advice.*# markowitz-portfolio-optimization

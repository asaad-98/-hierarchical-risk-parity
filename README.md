# Project Summary: Portfolio Optimization Using Hierarchical Risk Parity
Overview
In this project, we employ hierarchical risk parity (HRP) for portfolio optimization using data on S&P 500 constituents from 2015 to 2023. The data comprises asset prices without considering index rebalancing, reflecting the constituents as of 2024. The primary objective is to compare the performance of a portfolio optimized via HRP against a traditional equally weighted portfolio.

# Methodology
Data Preparation: We selected a subset of 100 randomly chosen assets from the S&P 500 index. Each asset's returns were calculated, and any returns smaller than a threshold of 1e-4 were set to zero to avoid computational issues in subsequent analyses.

# Portfolio Optimization:
In-Sample Data (up to 2018-01-05): We used this subset to optimize an HRP-based portfolio. The optimization considered maximum drawdown (MDD) as the risk measure and used hierarchical clustering (Ward's method) to diversify risk across different asset clusters.
Out-of-Sample Validation: The optimized weights were then applied to out-of-sample data (post-2018-01-05) to simulate real-world performance and robustness of the strategy.
Performance Comparison:
Both in-sample and out-of-sample returns were calculated for the optimized HRP portfolio and a baseline equally weighted portfolio.
We tracked and plotted daily returns to visualize the performance and drawdown periods of both portfolios.
Results
Enhanced Performance: The HRP portfolio generally outperformed the equally weighted portfolio, exhibiting higher Sharpe ratios and reduced drawdowns. This indicates better risk-adjusted returns, which can be attributed to the more sophisticated asset allocation approach that leverages the inherent hierarchical structure among the assets.
Risk Management: By implementing HRP, which considers not only the variances but also the correlations across different asset groups, the portfolio was better positioned to mitigate systemic risks and achieve lower volatility.

# Conclusion

The use of hierarchical clustering for portfolio optimization, specifically through the HRP method, demonstrated a clear advantage over simpler, equally weighted portfolio strategies. This project showcased how advanced statistical techniques could be effectively applied to enhance portfolio performance and risk management in financial markets. By adapting the hierarchical relationships within asset classes, HRP helps in distributing risk more evenly and capitalizing on diversification benefits that are not readily apparent through traditional asset allocation methods. After running a 100 experiments we achieve a mean increase in Sharpe of 0.02 in Sharpe, with up to 0.09 of increase possible. 


# Visual Representation and Documentation
The project included detailed visualizations to compare the cumulative returns and drawdown periods between the HRP-optimized portfolio and the equally weighted portfolio.
All analyses and findings were systematically documented in a Jupyter Notebook, making the study transparent and reproducible.
This project underscores the value of advanced portfolio optimization techniques in managing investment risks and improving returns, making it a valuable reference for financial analysts and portfolio managers looking to enhance their investment strategies using hierarchical clustering approaches.
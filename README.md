# End-to-End Systematic Equity Strategy

This notebook implements a complete systematic equity strategy pipeline:

1. **Data Loading & Preprocessing** - S&P 500 prices + Fama-French 5 factors
2. **Alpha Estimation** - Rolling FF5 regression to estimate stock alphas
3. **Feature Engineering** - Technical indicators and factor exposures
4. **Alpha Prediction** - ML models (ElasticNetCV, XGBoost, RandomForest, TabPFN)
5. **Risk Model** - Shrinkage covariance estimation
6. **Portfolio Optimization** - Multiple objectives (Max Sharpe, Target Risk, Target Return, etc.)
7. **Backtesting** - Weekly rebalancing with transaction costs
8. **Performance Analysis** - Strategy comparison and recommendation

**Configuration:**
- Date range: 2000-01-01 to 2020-11-24
- Training lookback: 260 weeks (~5 years)
- Rebalancing: Weekly (Friday)
- Universe: S&P 500 constituents

# Prince Chauhan

Senior Quantitative Researcher & Trader | Options, Volatility & Systematic Trading. New Delhi, India. 9+ years in Indian index derivatives; at SMC Global Securities since Dec 2024, trading the firm's proprietary capital and building its systematic trading platform. SEBI Registered Research Analyst. CA Final, Group 1 cleared.

I trade intraday Nifty and Sensex index options and F&O stocks with rule-based methods, and I build the research, backtest and risk code behind them. That code is private. The public pieces are here:

- [quant-research-portfolio](https://github.com/prince-chauhan-pc/quant-research-portfolio): small, tested Python versions of methods I use: backtesting with costs, SVI smiles with arbitrage checks, Johansen cointegration, volatility regimes tested out of sample, execution cost, Deflated Sharpe and Probability of Backtest Overfitting. All data there is synthetic.
- [CV (PDF)](https://github.com/prince-chauhan-pc/quant-research-portfolio/blob/main/docs/PC_CV/Prince%20Chauhan%20-%20Senior%20Quant%20Researcher%20and%20Trader.pdf)

## How I do research

- Costs before metrics. Charges come off each trade before any return, Sharpe ratio or drawdown is computed.
- No lookahead. A signal can only use data that existed when the trade was placed.
- Pass criteria are fixed before testing. Open-interest, crossover and market-view signals were tested over 3 years against a bar set in advance: right at least 55% of the time on moves of at least 0.05% within 60 minutes, and on the right side in each of the 3 years. None of them cleared it.
- Old results are re-tested under stricter rules. I re-ran six in-house strategy backtests (shared with the desk before deployment) with stops filled at the close of the trigger minute rather than at the stop price, no trades on days when India VIX was above 22, and no loss caps added after the fact.
  - Advance Straddle, with all three rules: backtest profit fell from INR 17.3 million to INR 5.84 million, about 66% lower.
  - Directional Options Selling, with the VIX and loss-cap rules (its stops still fill at the stop price): backtest profit fell from INR 17.0 million to INR 8.07 million, 53% lower.
  - Hourly Options Buying, Options Scalper and ORB Nifty Futures lost money after costs as coded.
  - The Bank Nifty basket was withdrawn because its code could not reproduce the original backtest result; the combined portfolio built on it was withdrawn too.

Stack: Python (pandas, NumPy, SciPy, scikit-learn), SQL, DuckDB, Parquet.

Contact: pchauhanrajput.pc@gmail.com

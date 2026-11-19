# Prince Chauhan

Senior Index Options Trader & Quant Researcher, New Delhi. Nifty, Bank Nifty and Sensex options. 9+ years in Indian index derivatives: research since 2017, trading SMC Global Securities' proprietary capital since Dec 2024. SEBI Registered Research Analyst. CA Final, Group 1 cleared.

I trade index options with rule-based methods and write the research, backtest and risk code behind them. That code is private. The public pieces are here:

- [quant-research-portfolio](https://github.com/prince-chauhan-pc/quant-research-portfolio): small, tested Python versions of methods I use. Backtesting with costs, SVI smiles with arbitrage checks, Johansen cointegration, volatility regimes tested out of sample, execution cost, Deflated Sharpe and Probability of Backtest Overfitting. All data there is synthetic.
- [CV (PDF)](https://github.com/prince-chauhan-pc/quant-research-portfolio/blob/main/docs/PC_CV/Prince%20Chauhan%20-%20Senior%20Quant%20Researcher%20and%20Trader.pdf)

## How I do research

- Costs before metrics. Charges come off each trade before any return, Sharpe ratio or drawdown is computed.
- No lookahead. A signal can only use data that existed when the trade was placed.
- Pass marks are set before testing. Open-interest, crossover and market-view signals were tested over 3 years against a mark fixed in advance: right at least 55% of the time on moves of at least 0.05% within 60 minutes, and on the right side in each of the 3 years. None of them cleared it.
- Re-test old results at stricter rules. I re-ran six of my published backtests and restated the two flagship ones at rules closer to live trading: stops filled at the close of the trigger minute, not at the stop price; no trades on days India VIX was above 22; no loss caps added after the fact.
  - Advance Straddle, with all three rules: INR 1.73 Cr fell to INR 58.35 L, a cut of about 66%.
  - Directional Options Selling, with the VIX and loss-cap rules (its stops still fill at the stop price): INR 1.70 Cr fell to INR 80.7 L, a cut of 53%.
  - Hourly Options Buying, Options Scalper and ORB Nifty Futures lose money after costs as coded.
  - The Bank Nifty basket was withdrawn because its code could not produce the published result. The combined portfolio built on it was withdrawn too.

Stack: Python (NumPy, SciPy, pandas), Parquet, pytest, Git.

Contact: [LinkedIn](https://www.linkedin.com/in/prince-chauhan-quant/) · pchauhanrajput.pc@gmail.com

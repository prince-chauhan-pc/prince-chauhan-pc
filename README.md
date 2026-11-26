# Prince Chauhan

**Senior Quant Researcher & Trader | Options, Futures & Equities | Systematic Trading**
New Delhi, India · SEBI Registered Research Analyst · CA Final, Group 1 cleared

Quantitative researcher and trader with 9+ years in index derivatives. At SMC Global Securities since Dec 2024, I lead a five-person team, trade the firm's rule-based proprietary book across NSE and BSE index options, futures, stock F&O and cash equities, and built the Python platform that runs it, from research and validation to risk and execution. I also built QuantsNerv, the India derivatives platform used across four SMC desks, and QuantsNervo, a US options and futures analytics and strategy platform, for SMC.

The trading, research and risk code is private. The public pieces are here:

- [quant-research-portfolio](https://github.com/prince-chauhan-pc/quant-research-portfolio): small, tested Python versions of methods I use: point-in-time options backtesting with costs, SVI smiles with arbitrage checks, Engle-Granger and Johansen cointegration, volatility regimes tested out of sample, execution cost, tear sheets, Deflated Sharpe and Probability of Backtest Overfitting. All data there is synthetic.
- [CV (PDF)](https://github.com/prince-chauhan-pc/quant-research-portfolio/blob/main/docs/PC_CV/Prince%20Chauhan%20-%20Senior%20Quant%20Researcher%20and%20Trader.pdf)

## How I do research

- **Costs before metrics.** Charges come off each trade before any return or risk figure is computed, and a strategy must still hold up at double costs.
- **No look-ahead.** Contracts, lot sizes and expiry days are taken as they stood on each date.
- **Pass criteria are fixed before testing.** Open-interest, crossover and market-view signals showed no standalone edge, so they are used only as context.
- **Old results are re-tested under stricter fill and risk rules.** The short-volatility and directional option-selling strategies stayed profitable with smaller returns, three other strategies failed to cover costs, and the Bank Nifty basket was withdrawn and rebuilt as a dispersion strategy that is now in forward testing.
- **New strategies earn their place.** They move from backtest to forward test to sandbox before they trade.
- **The order path is built for broker failures:** positions that lag fills, partial fills, timed-out orders and exchange freeze limits.

**Stack:** Python (pandas, NumPy, SciPy), SQL (PostgreSQL), real-time market data and broker APIs, LLM-assisted development with code review and safety gates.

**Contact:** pchauhanrajput.pc@gmail.com

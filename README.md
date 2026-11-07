# Prince Chauhan

Senior Quantitative Researcher & Systematic Derivatives Desk Lead — New Delhi, India.  
SEBI Registered Research Analyst · 9+ Years Derivatives Architecture · ~₹50 Cr Notional Capacity

[![Markets](https://img.shields.io/badge/Markets-India%20NSE%2FBSE%20%7C%20USA%20CBOE%20SPX-0284C7.svg)](#-dual-market-infrastructure)
[![Desk](https://img.shields.io/badge/Desk-24h%20Dual--Market%20Systematic-059669.svg)](#-dual-market-infrastructure)
[![Friction](https://img.shields.io/badge/Friction-0.50%25%20Per--Leg%20Drag-10B981.svg)](#-core-quant-invariants)
[![Showcase](https://img.shields.io/badge/Showcase-quant--research--portfolio-6366F1.svg)](https://github.com/prince-chauhan-pc/quant-research-portfolio)
[![CV](https://img.shields.io/badge/CV-Senior%20Quant%20Researcher-D97706.svg)](https://github.com/prince-chauhan-pc/quant-research-portfolio/blob/main/docs/PC_CV/Prince%20Chauhan%20-%20Senior%20Quant%20Researcher%20and%20Trader.pdf)

---

## 🏛️ Executive Summary

I architect and operate an institutional systematic options desk spanning Indian index derivatives (NSE Nifty, Bank Nifty, BSE Sensex) and USA volatility products (CBOE SPX, CME futures). 

With 9+ years on derivatives desks (SMC Global Securities, Smart Bulls Capital), my quantitative models manage ~₹50 Cr notional capacity with strict pre-trade risk controls, dynamic freeze-order slicing, and non-negotiable friction deductions on every leg.

- **Public Research Showcase**: **[`quant-research-portfolio`](https://github.com/prince-chauhan-pc/quant-research-portfolio)** — Tested Python implementations of production methods (SVI volatility surfaces, Johansen basket cointegration, K-means regime filters, execution latency simulation, and Deflated Sharpe overfitting gates).
- **Curriculum Vitae**: **[Download Institutional CV (PDF)](https://github.com/prince-chauhan-pc/quant-research-portfolio/blob/main/docs/PC_CV/Prince%20Chauhan%20-%20Senior%20Quant%20Researcher%20and%20Trader.pdf)**.

---

## 🌐 Dual-Market Infrastructure

The desk operates across two continuous sessions:

| Market | Operating Window (IST) | Core Products | Primary Feeds & Gateway |
|---|---|---|---|
| **India Desk** | 08:50 – 15:45 IST | Nifty 50, Bank Nifty, Sensex F&O | DhanHQ API v2 WebSocket, PreTrade RMS, Rule L25 Exit Escalator |
| **USA Desk** | 18:30 – 03:00 IST | CBOE SPX 0DTE/Multiday, CME ES/NQ | Databento OPRA L3 tick streams, Live GEX / Net Dealer Gamma |

---

## 🖥️ Workstation Topology

```mermaid
flowchart LR
    subgraph Execution["PC-2173 — Office Live Execution Node"]
        Dhan[DhanHQ WebSocket] --> Bus1[(Atomic Data Bus<br/>shared_data/)]
        Bus1 --> Bots1[India Systematic Bots]
        Bots1 --> RMS[Pre-Trade Risk Gate]
        RMS --> Fills[Broker Gateway]
    end

    subgraph Research["PC-2597 — Heavy Compute Cluster"]
        TickData[(Historical Parquet)] --> Harness[Master Backtest Harness]
        Harness --> MC[10,000 Monte Carlo Paths]
        MC --> Gate[Deflated Sharpe & Overfitting Gate]
    end

    subgraph US_Node["MacBook — USA Desk & Live Buying Node"]
        DataB[Databento OPRA Feed] --> GEX[Net Dealer Gamma Engine]
        GEX --> USBots[SPX Systematic Bots]
        USBots --> USPort[Port 5015 Dashboard]
    end

    Research -- Tested code via Git --> Execution
    Research -- Tested code via Git --> US_Node
```

---

## 🔬 Core Quantitative Invariants

1. **Non-Negotiable Friction Drag**: Every simulation charges a minimum 0.50% premium turnover friction on entry and exit legs before calculating metrics.
2. **Strict Intraday Capital Preservation (Rule L25)**: Intraday options positions face a 3-stage forced exit escalator starting at 15:20:00 IST to prevent overnight gap risk.
3. **No-Lookahead Guarantee**: Volatility regime sizing strictly enforces a one-bar lag. Zero contemporaneous information leakage.
4. **Exchange Freeze Slicing**: Automated order slicing across exchange freeze limits (1,800 Nifty / 900 Bank Nifty / 1,000 Sensex) with inter-slice pacing.
5. **Overfitting Deflation**: Backtest performance is audited against Bailey & Lopez de Prado's Deflated Sharpe Ratio (DSR) and Combinatorial Symmetric Cross-Validation (CSCV/PBO).

---

## 🛠️ Tech Stack

- **Core**: Python 3.12 (NumPy, SciPy, pandas, Polars).
- **Execution & Feeds**: asyncio, WebSockets, DhanHQ API v2, Databento L3 OPRA, Alpaca.
- **Data & Telemetry**: DuckDB, SQLite, Parquet, Flask, ReportLab PDF Tearsheets.
- **Testing & Risk**: pytest, unittest, GitHub Actions CI, Pre-Trade Risk Engine.

---

## 📬 Contact & Verification

- **Email**: pchauhanrajput.pc@gmail.com
- **LinkedIn**: [linkedin.com/in/prince-chauhan-quant](https://www.linkedin.com/in/prince-chauhan-quant/)
- **Location**: New Delhi, India

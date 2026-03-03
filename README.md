# BF.B Predictive Segment Tracker

Live interactive dashboard for Brown-Forman (BF.B) quarterly revenue forecasting with segment-level decomposition, peer correlation analysis, and backtest validation.

## Live Site

**[https://swolpump.github.io/bf-b-tracker/](https://swolpump.github.io/bf-b-tracker/)**

## Features

- **Segment Forecasting** — OLS regression with seasonal decomposition for Whiskey (~76%), Tequila (~7%), RTD (~11%), and Rest of Portfolio (~6%)
- **Composite Signal Scoring** — Google Trends (25%), Circana off-premise volume (30%), bourbon exports (15%), consumer confidence (15%), seasonal patterns (15%)
- **Peer Correlation Analysis** — Diageo, Suntory, Rémy Cointreau cross-validated against BF.B organic growth
- **Backtest Engine** — Rolling 1Q-ahead out-of-sample predictions across 6 quarters with MAPE, directional accuracy, and confidence intervals
- **Live Data Refresh** — One-click pull from Yahoo Finance, FMP, Google Trends, FRED, and NewsAPI via CORS proxy

## Model Performance

| Metric | Value |
|--------|-------|
| Backtest MAPE | 1.14% |
| Directional Accuracy | 83% |
| Mean Forecast Error | $11M |
| 90% Confidence Interval | ±$28M |

## Data Sources

- Yahoo Finance (BF.B price data)
- Financial Modeling Prep (quarterly financials)
- Google Trends (brand interest indices)
- FRED (consumer confidence, economic indicators)
- DISCUS (bourbon export data)
- Circana (off-premise volume proxy)
- NewsAPI (sentiment signals)

## Technical Stack

Single-file HTML dashboard (~69KB) with Chart.js 4.4.1 and chartjs-plugin-annotation. No build step required.

## Deploy

Hosted via GitHub Pages. To run locally, simply open `index.html` in a browser.

## Brown-Forman Fiscal Calendar

Brown-Forman's fiscal year ends April 30. Q1 = May–Jul, Q2 = Aug–Oct, Q3 = Nov–Jan, Q4 = Feb–Apr.

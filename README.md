# Nifty Pharma Comprehensive Research Dashboard

Interactive single-file HTML dashboard for analyzing Nifty Pharma stocks using the 40-parameter qualitative research dataset.

## Overview

This dashboard combines:

- **Live price charts** (candlesticks, volume, moving averages) via TradingView
- **Extracted quantitative metrics** (growth, EBITDA margins, ROCE, P/E, PEG, promoter holding, quality scores)
- **Peer comparison tables**, heatmaps, scatter plots, and radar charts
- **Full searchable research notes** from the original CSV

It follows the requested analysis flow:

**Price + Candlesticks → Volume → Moving Averages → Returns / Volatility Proxies → Fundamentals → Peer Comparison**

## Features

| Tab | Description |
|-----|-------------|
| **1. Price + Candles + Volume + MAs** | Live TradingView Advanced Chart for any selected NSE Pharma stock. Includes candlesticks, volume bars, and 20/50/200-day moving averages. |
| **2. Returns / Volatility Proxies** | Bar charts of historical growth CAGR and EBITDA margin ranges. Thesis-breaker risk table with qualitative risk levels. |
| **3. Fundamentals Snapshot** | Card view of key metrics for every company (growth, margins, ROCE, valuation, debt, promoter holding, quality score). |
| **4. Peer Comparison & Heatmap** | Sortable-style comparison table + quality / promoter holding visualization. |
| **5. Risk-Return & Quality Scores** | Scatter plot (ROCE vs P/E) and interactive radar chart for business quality dimensions. |
| **6. Full Research Notes** | Searchable view of the original qualitative research text for all companies. |

## Supported Companies

DIVISLAB, SUNPHARMA, DRREDDY, ZYDUSLIFE, LAURUSLABS, GLENMARK, AUROPHARMA, TORNTPHARM, LUPIN, CIPLA, ALKEM, MANKIND, GLAND, BIOCON, AJANTPHARM, ABBOTINDIA, IPCALAB, WOCKPHARMA

## How to Use

1. Download / save the file as `nifty-pharma-dashboard.html`
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari)
3. Internet connection is required only for:
   - TradingView widget (live charts)
   - Chart.js CDN
4. Use the top tabs to navigate between views
5. In the Price tab, select a stock from the dropdown and click **Load Chart**

No build step, no server, no installation required.

## Data Source & Limitations

**Source**: `Nifty_Pharma_Comprehensive_Research_1_to_40.csv`  
(40 qualitative parameters covering financials, pipeline, regulatory, valuation, governance, etc.)

**Important limitations**:

- The CSV contains **text descriptions only** — no historical OHLC, volume, or time-series price data.
- All numerical ranges (growth %, EBITDA %, ROCE, P/E, PEG) were **manually extracted and mid-pointed** from the qualitative notes.
- Quality scores (1–10) are composite judgments derived from the research text.
- Real candlestick / volume / moving-average charts are supplied by the **TradingView widget**, not from the CSV.
- For fully offline historical price analysis you must pre-download OHLCV data (e.g. via `yfinance` or NSE) and embed it.

## Tech Stack

- Pure HTML + CSS + JavaScript (single file)
- [Chart.js](https://www.chartjs.org/) – bar, scatter, radar charts
- [TradingView Advanced Chart Widget](https://www.tradingview.com/widget/) – live candlesticks, volume, MAs
- No frameworks, no build tools, no backend

## File Structure


## Possible Enhancements

- Embed actual historical OHLCV arrays for offline candlestick / drawdown / relative-performance charts
- Add downloadable Excel/PDF export of the peer comparison table
- Implement client-side sorting and filtering on the peer table
- Add more companies or refresh the qualitative scores from updated research
- Connect to a live fundamentals API for real-time P/E, market cap, etc.
- Dark/light theme toggle

## License

This dashboard is provided for research and educational purposes.  
TradingView widget usage is subject to TradingView’s terms.  
Original research data remains the property of its source.

---

**Created for Nifty Pharma qualitative research analysis**  
October 2026



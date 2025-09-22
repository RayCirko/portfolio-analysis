# Portfolio Performance Analysis vs S&P 500

![Python](https://img.shields.io/badge/python-3.10-blue)
![License](https://img.shields.io/badge/license-MIT-green)

This project analyzes the performance of a hypothetical stock portfolio compared to the S&P 500 benchmark. It demonstrates practical financial analysis, portfolio construction, and data visualization skills using Python and yfinance.
## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Example Output](#example-output)
- [SQL Analysis](#sql-analysis)
- [Key Insights](#key-insights)
- [Author](#author)
## Features
- Download and clean 5 years of stock price data (S&P 500 constituents)  
- Calculate daily returns, annualized returns, and volatility  
- Compute **Sharpe Ratios** to rank stocks by risk-adjusted performance  
- Build a portfolio of the top 10 stocks based on Sharpe Ratio  
- Visualize:
  - Risk vs Reward (Volatility vs Return)  
  - Portfolio Allocation Pie Chart  
  - Portfolio Cumulative Returns over time  
  - Portfolio vs S&P 500 ETF (SPY) comparison  
- Generate final tables for SQL analysis (`portfolio_summary.csv`, `portfolio_daily_returns.csv`, `spy_price.csv`)  

## Technologies Used
- Python 3.10
- Pandas  
- NumPy  
- Matplotlib / Seaborn  
- yfinance  
- Plotly (optional for interactive charts)  

## Project Structure
```
portfolio-analysis/
    data/
        portfolio_summary.csv         # Portfolio summary output
        portfolio_daily_returns.csv   # Portfolio daily returns output
        spy_price.csv                 # Benchmark (SPY) data
        sp500_tickers.csv (optional)  # Optional: static list of S&P 500 tickers
        query1_portfolio_vs_spy.txt   # SQL query for Portfolio vs SPY
        query2_monthly_aggregates.txt # SQL query for monthly aggregates
        query3_top_contributors.txt   # SQL query for top contributors
    figures/
        figure1_portfolio_vs_spy.png
        figure2_monthly_aggregates.png
        figure3_top_contributors.png
    sp500_portfolio_analysis.ipynb    # Main Jupyter Notebook
    requirements.txt                  # List of Python dependencies
    README.md                         # Project documentation
```
> **Note:** The raw S&P 500 historical stock prices file (`sp500_prices_all.csv`) is too large to include in the repo.  
> Running `sp500_portfolio_analysis.ipynb` will automatically download the latest S&P 500 data from Yahoo Finance.

## Getting Started

1. Clone the repository:
    git clone https://github.com/RayCirko/portfolio-analysis.git
    cd portfolio-analysis

2. Install dependencies:
    pip install -r requirements.txt

3. Open `sp500_portfolio_analysis.ipynb` in Jupyter Notebook or Google Colab.  
4. Run the notebook; all outputs will save in the `data/` folder.

> **Optional:** The `sp500_tickers.csv` file provides a static list of tickers for offline use. The notebook will also fetch the latest tickers automatically from DataHub if this file is not present.

## Example Output
Portfolio vs S&P 500 (Cumulative Return)  
<img width="1001" height="701" alt="image" src="https://github.com/user-attachments/assets/b66d726b-854a-4aec-a65a-0a5a6617a301" />

---

## SQL Analysis

### Figure 1: Portfolio vs SPY Cumulative Returns

**Query:** See `data/query1_portfolio_vs_spy.txt`  
**Result:** Screenshot: `figures/figure1_portfolio_vs_spy.png`  

This query shows the daily cumulative returns of your portfolio compared to the S&P 500 ETF (SPY).

### Figure 2: Monthly Aggregates of Portfolio

**Query:** See `data/query2_monthly_aggregates.txt`  
**Result:** Screenshot: `figures/figure2_monthly_aggregates.png`  

This query calculates monthly averages of daily returns and cumulative returns, providing insights into month-to-month portfolio performance trends.

### Figure 3: Top 5 Weighted Return Contributors

**Query:** See `data/query3_top_contributors.txt`  
**Result:** Screenshot: `figures/figure3_top_contributors.png`  

This query lists the top 5 portfolio tickers contributing the most to overall return. It highlights which holdings drive the portfolio’s performance.

## Key Insights
- The top 10 portfolio stocks had higher Sharpe Ratios than the S&P 500 average.
- Apple (AAPL) and Microsoft (MSFT) were the largest contributors to portfolio returns.
- Monthly analysis revealed seasonal volatility patterns, with higher returns in Q4.

---

## Author
Ray Cirko  
Email: rayxcirko@gmail.com  
LinkedIn: https://www.linkedin.com/in/ray-c-786074110/  
GitHub: https://github.com/RayCirko


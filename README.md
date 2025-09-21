# Portfolio Performance Analysis vs S&P 500

This project analyzes the performance of a hypothetical stock portfolio compared to the **S&P 500** benchmark.  
It uses Python, `yfinance` for data collection, and standard financial metrics for performance evaluation.

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
├── data/
│   ├── portfolio_summary.csv         # Portfolio summary output
│   ├── portfolio_daily_returns.csv   # Portfolio daily returns output
│   ├── spy_price.csv                 # Benchmark (SPY) data
│   └── sp500_tickers.csv (optional)  # Optional: static list of S&P 500 tickers
├── sp500_portfolio_analysis.ipynb    # Main Jupyter Notebook
├── requirements.txt                  # List of Python dependencies
└── README.md                         # Project documentation
```
> **Note:** The raw S&P 500 historical stock prices file (`sp500_prices_all.csv`) is too large to include in the repo.  
> Running `sp500_portfolio_analysis.ipynb` will automatically download the latest S&P 500 data from Yahoo Finance.


## Example Output
Portfolio vs S&P 500 (Cumulative Return)  


## Author
Ray Cirko
rayxcirko@gmail.com  
LinkedIn: https://www.linkedin.com/in/ray-c-786074110/ <br>
GitHub: https://github.com/RayCirko 


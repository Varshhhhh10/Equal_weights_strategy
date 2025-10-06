# 🎯 Top 10 Nifty Stocks: Simple Equal-Weight Portfolio Allocation

## Project Overview

This project provides a straightforward, automated method for fetching the latest price and fundamental data for a basket of stocks, selecting the top 10 largest companies by market capitalization, and calculating the number of shares to buy for a simple equal-weight investment strategy.

The goal is to demonstrate core Python and data science library skills in a practical financial application.

## 🔑 Key Functionality

The script performs the following steps:

1.  **Data Acquisition:** Downloads the latest closing price and current market capitalization for a predefined list of stock tickers (Nifty constituents).
2.  **Ranking:** Sorts the fetched stocks based on their **Market Capitalization** in descending order.
3.  **Selection:** Filters the list to retain only the **Top 10** largest companies (Large-Cap bias).
4.  **Equal-Weight Allocation:** Calculates a fixed `position_size` by dividing the total portfolio amount by the number of selected stocks (10).
5.  **Share Calculation:** Determines the maximum **whole number of shares** that can be purchased for each of the top 10 stocks, ensuring the budget for each position is not exceeded.

## 🛠️ Technical Stack

  * **Programming Language:** Python
  * **Data Manipulation:** Pandas, NumPy
  * **Data Sourcing:** `yfinance` (for stock price and fundamental data)
  * **Mathematical Operations:** `math`

## ⚙️ How the Allocation Works

The core of the allocation logic is ensuring an exact, equal distribution of funds across the chosen stocks while only buying whole shares.

$$\text{Position Size} = \frac{\text{Portfolio Size}}{\text{Number of Stocks (10)}}$$

$$\text{Number of Shares to Buy} = \text{FLOOR} \left( \frac{\text{Position Size}}{\text{Latest Price}} \right)$$

The `math.floor()` function is crucial here, as it ensures all calculations result in a valid integer number of shares.

## 🚀 Getting Started

To run this project, you need Python and the necessary libraries installed.

### 1\. Installation

```bash
pip install pandas numpy yfinance
```

### 2\. Prepare Data Input

Ensure you have a variable or DataFrame accessible in your environment named `ticker` (as per the line `tickers_list=ticker["Ticker"].values.tolist()`) that contains a column named `"Ticker"` with the stock symbols you want to analyze.

### 3\. Execution

Execute the code in a Jupyter Notebook cell. The script will:

1.  Ask the user for the total investment amount (`portfolio_size`).
2.  Print the final DataFrame showing the `Market Cap`, `Latest Price`, and the calculated `Number of shares to buy` for the Top 10 stocks.
    pip install pandas numpy matplotlib yfinance
    ```
3.  **Run the notebook:** Open `Equal_weights_strategy.ipynb` in VS Code or Jupyter Lab and execute the cells sequentially.

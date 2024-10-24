# Financial-Portfolio-Evaluation-System

This project is designed to evaluate and optimize investment portfolios using advanced financial analysis techniques such as Monte Carlo Simulation and Bollinger Band strategies. It aims to provide actionable insights for asset allocation and risk management based on both historical and real-time data.

## Features

- **Monte Carlo Simulation**: Used to forecast the probability of different outcomes in a process that cannot easily be predicted due to the intervention of random variables.
- **Bollinger Bands**: A technical analysis tool defined by a set of trendlines plotted two standard deviations (positively and negatively) away from a simple moving average (SMA) of a security's price.
- **Moving Average Crossover Strategies**: Includes both flat and short strategies to determine trading signals based on moving averages.
- **Performance Metrics**: Calculates key performance indicators such as Sharpe Ratio, Maximum Drawdown, and Success Ratio for portfolio evaluation.

## Installation

To set up the project, ensure you have Python installed along with the required libraries:

```bash
pip install pandas numpy matplotlib statsmodels
```

## Usages
Load Price Data: Use the read_price_data function to load your historical price data from a CSV file.

```bash
prices = read_price_data('PricesProjectA.csv')
Run Strategies: Utilize the runMovingAverageAndBB function to execute both Moving Average and Bollinger Band strategies.
```

```bash
results = runMovingAverageAndBB(prices[['AAPL']], maFast=31, maSlow=222, bbWindow=20, stdevBand=3)
Evaluate Performance: Calculate performance statistics using calcPerformanceStatistics.
```

```bash
performance_stats = calcPerformanceStatistics(results)
Optimize Portfolio: Use the getOptimalMAWindows and getOptimalBBWindows functions to find the optimal parameters for your strategies.
```

### Parameters
* maFast: 31
* maSlow: 222
* bbWindow: 20
* bbStdevBand: 3
* Strategies and Securities

The system evaluates various strategies including:

* 'AAPL-MAFlat'
* 'AMZN-BMK-MA'
* 'ATT-BB'
* 'EUR-MAShort'
* 'FBNDX-MAShort'
* 'GE-MAShort'
* 'GOLD-MAShort'
* 'SPY-MAFlat'


These strategies are selected based on their Sharpe ratios to ensure optimal performance across different market conditions.

## Example Analysis
The project includes an example analysis where the Sharpe ratio for each strategy is calculated, and an optimal portfolio is constructed with a Sharpe ratio exceeding 1. This demonstrates the system's capability to enhance portfolio returns while managing risk effectively.

## Contribution
Contributions are welcome! Please fork the repository and submit a pull request with your improvements or additional features.

# ES-HyperNEAT Stock Trading

This Python project implements an Evolvable Substrate HyperNEAT (ES-HyperNEAT) approach to evolve stock trading strategies using the NEAT (NeuroEvolution of Augmenting Topologies) algorithm and PurePLES library.

## Features

- Uses ES-HyperNEAT to evolve neural network topologies for stock trading
- Fetches historical stock data using yfinance
- Implements a stock portfolio simulation
- Compares evolved strategies against a buy-and-hold benchmark
- Visualizes portfolio performance over time

## Requirements

- Python 3.x
- numpy
- pandas
- yfinance
- neat-python
- pureples
- matplotlib

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/es-hyperneat-stock-trading.git
   ```
2. Install the required packages:
   ```
   pip install numpy pandas yfinance neat-python pureples matplotlib
   ```

## Usage

1. Ensure you have a NEAT configuration file named `config-feedforward` in the project directory.
2. Run the script:
   ```
   python es_hyperneat_stock_trading.py
   ```

The script will:
1. Fetch historical stock data for the specified symbols
2. Train the ES-HyperNEAT model on the training data
3. Test the best evolved strategy on the test data
4. Compare the results with a buy-and-hold strategy
5. Generate a plot of the results

## How it Works

1. `StockHistoryService`: Fetches and manages historical stock data.
2. `StockPortfolio`: Simulates a stock portfolio, handling buying, selling, and value calculation.
3. `ESHyperNEATTrader`: Implements the ES-HyperNEAT algorithm for evolving trading strategies.
4. The main script runs the experiment, including training, testing, and visualization.

## Key Components

- `ESHyperNEATTrader`: Manages the evolution of trading strategies.
- `evaluate`: Fitness function for evaluating genome performance.
- `test_agent`: Tests the best evolved agent on unseen data.
- `buy_and_hold`: Implements a simple buy-and-hold strategy for comparison.
- `plot_results`: Visualizes the performance of evolved strategies vs. buy-and-hold.

## Customization

You can adjust the following parameters in the script:
- `symbols`: List of stock symbols to trade
- `lookback_days`: Number of past days to consider for decision making
- `cppn_mode`: CPPN mode (currently set to '2d')
- `evaluations_per_agent`: Number of evaluations per agent for more robust fitness assessment

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Inspiration

This project was inspired by a github repo https://github.com/Bitjieff/cryptochronolonic

## Disclaimer

This code is far from perfect. Please feel free to improve. (it took me a long time to understand ES Hyperneat, and still working on it...)

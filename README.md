 # Algorithmic Trading Platform

A Python-based algorithmic trading platform that integrates with Zerodha for automated trading strategies. The platform provides a comprehensive set of technical indicators and backtesting capabilities.

## 🚀 Quick Start

1. Clone the repository:
```bash
git clone https://github.com/yourusername/algotrading.git
cd algotrading
```

2. Set up the environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

3. Configure Zerodha credentials and trading parameters

## 📊 Technical Indicators

The platform includes the following technical indicators:

| Indicator | Description | Implementation |
|-----------|-------------|----------------|
| EMA | Exponential Moving Average | `indicators/EMA.py` |
| MACD | Moving Average Convergence Divergence | `indicators/MACD.py` |
| RSI | Relative Strength Index | `indicators/RSI.py` |
| ATR | Average True Range | `indicators/ATR.py` |
| MFI | Money Flow Index | `indicators/MFI.py` |
| SuperTrend | Trend-following indicator | `indicators/SuperTrend.py` |
| VWAP | Volume Weighted Average Price | `indicators/VWAP.py` |

## 📁 Project Structure

```
algotrading/
├── data/                   # Data storage and configuration
├── indicators/             # Technical analysis indicators
│   ├── ATR.py             # Average True Range
│   ├── EMA.py             # Exponential Moving Average
│   ├── MACD.py            # Moving Average Convergence Divergence
│   ├── MFI.py             # Money Flow Index
│   ├── RSI.py             # Relative Strength Index
│   ├── SuperTrend.py      # SuperTrend indicator
│   └── VWAP.py            # Volume Weighted Average Price
├── zerodha/               # Zerodha trading integration
│   ├── backtest.py        # Backtesting functionality
│   ├── setup.py           # Trading setup and configuration
│   └── ema_crossover.py   # EMA Crossover strategy
└── requirements.txt       # Python dependencies
```

## 💻 Usage

### Running a Strategy
```python
from zerodha import setup
from indicators import RSI, MACD

# Initialize trading setup
trading_setup = setup.initialize()

# Example: EMA Crossover Strategy
from zerodha.ema_crossover import EMACrossover
strategy = EMACrossover()
strategy.run()
```

### Backtesting
```python
from zerodha import backtest

# Run backtest on historical data
backtest.run(strategy, start_date='2023-01-01', end_date='2023-12-31')
```

## 🛠 Development

### Adding New Indicators
1. Create a new file in `indicators/`
2. Follow the existing pattern:
   - Use type hints
   - Add comprehensive docstrings
   - Include error handling
3. Add tests in `tests/`

### Testing
```bash
pytest
```

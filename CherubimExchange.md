# Cherubin Exchange: Portfolio Evaluation & Trading Simulation

Cherubin Exchange is a modular, extensible framework designed to simulate financial market dynamics and evaluate the performance of automated trading strategies. The project provides a sandboxed environment where various trading agents—from simple noise traders to complex institutional execution algorithms—interact within a simulated order book.

## Overview

The goal of Cherubin Exchange is to bridge the gap between theoretical strategy development and realistic market execution. By simulating not just price movement, but the underlying order book mechanics, PETS allows developers to observe how strategies impact market liquidity and respond to different volatility regimes.

## Key Features

- **Multi-Agent Simulation**: Support for diverse trader archetypes (Noise, Trend Followers, Market Makers, Mean Reversion, etc.).
- **Order Book Dynamics**: A centralized exchange simulation that handles limit and market orders.
- **Pluggable Strategies**: An abstract interface for implementing and testing custom trading logic.
- **Risk Management Engine**: Built-in safeguards to monitor margin, position limits, and drawdowns (now implemented).
- **Performance Analytics**: Detailed tracking of Sharpe Ratio, Max Drawdown, PnL per agent, and comparative ranking with individual trader details and thematic icons.

## Project Structure

```text
Cherubin Exchange/
├── simulation/          # Core simulation engine and exchange logic
│   ├── traders/         # Agent implementations (Noise, Trend Followers, etc.)
│   ├── risk_manager.py  # Risk management engine with margin/position/drawdown controls
│   ├── mean_reversion_trader.py  # Mean reversion strategy trader
│   ├── trend_follower_trader.py  # Trend following strategy trader
│   ├── engine.py        # Orchestrates the simulation loop
│   └── exchange.py      # Order book and matching logic
├── analytics/           # Evaluation metrics and visualization tools
├── data/                # Historical data and synthetic generators
└── tests/               # Unit and integration tests
```

## Getting Started

1. Install dependencies: `pip install -r requirements.txt`
2. Run the simulation: `streamlit run app.py`
3. View risk management demo: `python demo_risk.py`
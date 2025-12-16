# UK Electricity Market Simulation

A Python simulation of the UK electricity market pay-as-clear auction mechanism, computing hourly electricity prices and generation mix for a 7-day period (168 hours).

## Overview

Generators bid their marginal cost into the market. The system operator dispatches them from cheapest to most expensive until demand is met. The last generator dispatched sets the clearing price for all participants.

The simulation models:
- Wind and solar plants with £0 marginal cost (variable availability based on load factors)
- Gas plants with costs determined by gas price and plant efficiency

## Project Structure
```
├── data/
│   └── data 2.xlsx                      # Input data (plants, load factors, demand, gas prices)
├── images/                              # Methodology diagram and flowchat
│   ├── Merit_Order_Example__How_Marginal_Price_is_Determined.png
│   └── UK_Electricity_Market_Dispatch_Algorithm_-_Step-by-Step_Process.png
├── notebooks/
│   └── electricity_market_simulation.ipynb   # Main analysis
├── results/
│   ├── simulation_results.csv           # Hourly results (168 rows)
│   ├── 01_exploratory_analysis.png      # Visualizations
│   ├── 02_electricity_price_over_time.png
│   ├── 03_generation_mix.png
│   └── 04_merit_order_curves.png
├── Technical Interview Quant Dev.pdf    # Assessment brief
├── requirements.txt
└── README.md
```

## Data

| Asset Type | Count | Total Capacity |
|------------|-------|----------------|
| Wind plants | 6 | 22,500 MW |
| Solar plants | 10 | 26,000 MW |
| Gas plants | 5 | 17,500 MW |

Time series: 168 hours of demand, gas prices, and green energy load factors.
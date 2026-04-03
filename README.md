# Monte Carlo Stock Price Simulation

## Overview

Simulates future stock price paths using a Monte Carlo method grounded in Geometric Brownian Motion (GBM). Given a historical price series for any ticker, the model generates thousands of possible price trajectories over a one-year trading horizon and plots the distribution of outcomes.

## Methodology

The project models stock returns as a continuous-time random walk with drift — Geometric Brownian Motion. Daily log returns are computed from historical closing prices and used to estimate two parameters: the drift term (expected return adjusted for variance) and volatility (standard deviation of log returns). Future daily returns are then generated using the GBM formula:

$$
\frac{S(t)}{S(t-1)} = e^{\left(\mu - \frac{\sigma^2}{2}\right)\Delta t + \sigma\sqrt{\Delta t} \cdot Z}
$$

where $Z$ is drawn from a standard normal distribution via the inverse CDF. The simulation runs 10,000 iterations over 251 trading intervals (one year). As iterations increase, the mean of simulated paths converges toward the drift-implied expected value.

## Language

Python

## Requirements

Install dependencies using: pip install -r requirements.txt

Clone the repository
Install dependencies: pip install -r requirements.txt
Open MonteCarlo_DifferentPaths.ipynb in Jupyter
Set your desired ticker, start_date, and end_date in Cell 3
Run all cells in order — the final plot displays all simulated price paths


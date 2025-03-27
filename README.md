# Asset Pricing Project (2024/25)

This project was developed as part of the MSc Quantitative Finance/Mathematical Trading and Finance/Financial Mathematics programme at Bayes Business School (formerly Cass). It received the highest mark in the cohort. The work applies forecasting models and mean-variance portfolio optimisation to evaluate long-term investment strategies over a ten-year period.

## Overview

The core objective is to assess whether semi-annual forecasts of market returns can enhance portfolio performance relative to traditional passive strategies. The analysis combines volatility modelling with dynamic portfolio construction, and compares the terminal outcomes across a range of strategies.

The project is structured around four main components:

1. **Forecasting Model** — Predicts whether to invest in the market or risk-free asset every six months using an EGARCH volatility framework.
2. **Portfolio Construction** — Builds efficient frontiers and selects market/minimum-variance portfolios using five UK equities.
3. **Terminal Wealth Simulation** — Evaluates the performance of seven distinct strategies over a 10-year horizon (2014–2024).
4. **Client Report** — Summarises findings and provides investment recommendations in a clear, non-technical format.

## Repository Structure

```
Asset-Pricing-Project/
├── DataAnalysis_EfficientFrontiers.ipynb   # Main analysis notebook
├── Client-Facing-Report.pdf                # Final report (submitted)
├── datasets/                               # Raw and processed data
├── Images/                                 # Plots and visualisations
├── Task.pdf                                # Coursework brief
└── README.md
```

## Summary of Results

| Strategy                                  | Terminal Wealth (£) | CAGR   |
|-------------------------------------------|----------------------|--------|
| Forecasting Model-Guided Portfolio        | 1,497.35             | 4.12%  |
| Minimum Variance (No Rebalancing)         | 1,420.43             | 3.57%  |
| Market Portfolio (Rebalanced)             | 1,322.73             | 2.81%  |
| FTSE All Share Index                      | 1,264.99             | 2.33%  |
| UK 1-month Government Bonds               | 1,137.98             | 1.32%  |

> The model-guided strategy outperformed all benchmarks, including the FTSE All Share index, over the investment period.

## How to Run

Clone the repository and launch the notebook:

```bash
git clone https://github.com/RemaniSA/Asset-Pricing-Project.git
cd Asset-Pricing-Project
pip install pandas numpy matplotlib scipy arch
jupyter notebook DataAnalysis_EfficientFrontiers.ipynb
```

The project was developed in Python 3 and tested in Jupyter Notebook.

## Methods

- **EGARCH Forecasting**: Used to estimate semi-annual return distributions. Allocation was based on whether expected returns exceeded the risk-free rate.
- **Mean-Variance Optimisation**: Rolling construction of efficient frontiers using five UK stocks: AstraZeneca, BAT, Bunzl, National Grid, and Vodafone.
- **Strategy Evaluation**: Compared both rebalanced and buy-and-hold versions of market and min-variance portfolios, along with benchmark indices and a forecast-driven strategy.

## Authors

- Shaan Ali Remani  
- Gael Chen  
- Fabrice Sashinkumar  

# Coursework Brief

![Asset Pricing Page 1](https://github.com/RemaniSA/Asset-Pricing-Project/blob/main/Images/Final_Coursework_AP_Page_1.jpeg)

![Asset Pricing Page 2](https://github.com/RemaniSA/Asset-Pricing-Project/blob/main/Images/Final_Coursework_AP_Page_2.jpeg)

# Asset Pricing Project

This project was developed as part of the MSc Mathematical Trading and Finance programme at Bayes Business School (formerly Cass). It combines volatility forecasting and dynamic asset allocation to construct a long-term investment strategy, benchmarked against the FTSE All Share Index and other portfolio strategies over a 10-year period.

## Problem

The central challenge was to evaluate whether a forecasting-driven allocation strategy could outperform traditional passive or heuristic-based approaches. Using an EGARCH(1,1) model to predict equity market volatility, the project dynamically shifted capital between equities and risk-free gilts. Portfolio construction followed a mean-variance framework, with semi-annual rebalancing informed by forecast signals.

## My Reflections

This was my first real coding project, and learning to take raw Python skills into a full investment simulation was both rewarding and formative. It taught me that good inputs alone aren't enough; we also need to understand when and where models perform best. Ours relied on a macroeconomic indicator, and with more time I would have explored how to fuse it with micro-level factors into a global, regime-aware forecasting system. One insight that really stuck: rebalancing isn't always good. The difference in performance between strategies that rebalanced at set intervals versus those guided by market signals was substantial. This project shifted how I think about portfolio design and made me appreciate the link between model signal quality and rebalancing discipline.

## Methods

- Volatility Forecasting: EGARCH(1,1) model to guide allocation shifts
- Asset Universe: 5 uncorrelated UK equities selected via Sharpe Ratio analysis
- Portfolio Construction: Mean-variance optimisation to construct frontier
- Allocation Logic: Semi-annual rebalancing based on forecasted risk regime
- Benchmarking: Compared against passive market, minimum variance, and FTSE index strategies

## Repository Structure

```
Asset-Pricing-Project/
├── Images/
├── datasets/
├── .gitignore
├── Client-Facing-Report.pdf
├── DataAnalysis_EfficientFrontiers.ipynb
├── README.md
├── Task.pdf
```

## Summary of Results

| Strategy                                  | Terminal Wealth (£) | CAGR   |
|-------------------------------------------|----------------------|--------|
| Forecasting Model-Guided Portfolio        | 1,497.35             | 4.12%  |
| Minimum Variance (No Rebalancing)         | 1,420.43             | 3.57%  |
| Market Portfolio (Rebalanced)             | 1,322.73             | 2.81%  |
| FTSE All Share Index                      | 1,264.99             | 2.33%  |
| UK 1-month Government Bonds               | 1,137.98             | 1.32%  |

> The model-guided portfolio outperformed all benchmarks, illustrating the value of adaptive allocation informed by volatility forecasting.

## Requirements

```bash
pip install pandas numpy matplotlib scipy arch
```

Project developed in Python 3 and run in Jupyter Notebook.

## How to Run

```bash
git clone https://github.com/RemaniSA/Asset-Pricing-Project.git
cd Asset-Pricing-Project
jupyter notebook DataAnalysis_EfficientFrontiers.ipynb
```

Ensure all datasets are placed in the `/datasets` folder and figures are saved to `/Images`.

## Further Reading

- Cuthbertson, K. & Nitzsche, D.: *Investments. Second Ed.*
- Tsay, R.: *Analysis of Financial Time Series*
- Meucci, A.: *Risk and Asset Allocation*

## Authors

- Shaan Ali Remani  
- Gael Chen  
- Fabrice Sashinkumar

---

### Connect

- [LinkedIn](https://www.linkedin.com/in/shaan-ali-remani)  
- [GitHub](https://github.com/RemaniSA)

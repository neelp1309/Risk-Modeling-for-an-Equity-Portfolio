# 📊 Risk Modeling for an Equity Portfolio

This project implements a quantitative risk model for a portfolio of publicly traded equities, focusing on risk estimation and analysis using statistical and financial metrics. It is designed to replicate real-world processes used by portfolio managers, risk analysts, and financial institutions to evaluate the potential downside exposure of investment strategies.

---

## 📌 Objectives

- Quantify portfolio-level risk using historical market data
- Compute key risk metrics such as **Volatility**, **Value-at-Risk (VaR)**, and **Conditional Value-at-Risk (CVaR)**
- Visualize risk distributions, time-based volatility trends, and asset correlations
- Prepare risk analytics and visual outputs suitable for reporting or dashboarding
- Enable extension into backtesting, stress testing, and real-time monitoring

---

## 🔍 Project Scope

The model is built using Python and utilizes market data from **Yahoo Finance**. The following key features are implemented:

- ✅ **Portfolio Construction**  
  Equal-weighted portfolio of selected equities (`AAPL`, `MSFT`, `GOOGL`, `TSLA`) with customizable weights

- ✅ **Statistical Risk Estimation**  
  - Annualized volatility  
  - 95% Parametric VaR (based on normal distribution)  
  - 95% Conditional VaR (average of tail losses)

- ✅ **Data Visualization**  
  - Distribution of returns with VaR overlay  
  - Rolling volatility plot  
  - Correlation heatmap of asset returns  

- ✅ **Automation Ready**  
  - Modular code for integration into risk reporting pipelines  
  - Scalable design to include more assets or alternative data sources

---

## 📁 Project Structure

```
risk-model-equity-portfolio/
│
├── notebooks/            # Jupyter notebooks (main implementation)
├── data/                 # Optional folder for saved historical data
├── visuals/              # Saved plots and output charts
├── requirements.txt      # Python dependencies
├── .gitignore            # Files to ignore
└── README.md             # Project overview (this file)
```

---

## 📈 Data Source

Historical daily adjusted close prices are retrieved from:

> [Yahoo Finance](https://finance.yahoo.com)

via the `yfinance` API, covering a 3-year window for major tech equities. Users can easily modify tickers and timeframes for custom portfolios.

---

## 🧠 Technologies & Tools

- **Python**: Core language
- **Pandas, NumPy**: Data processing
- **SciPy**: Statistical modeling
- **Matplotlib, Seaborn, Plotly**: Visualization
- **yfinance**: Financial data extraction
- **Google Colab**: Development environment

---

## 🧮 Key Risk Metrics

| Metric       | Description |
|--------------|-------------|
| Volatility   | Standard deviation of daily returns annualized (× √252) |
| VaR (95%)    | Maximum expected loss at 95% confidence under normal distribution |
| CVaR (95%)   | Expected loss beyond the 95% VaR threshold (average tail loss) |

---

## 📌 How to Use

1. Clone the repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Run the notebook:
```bash
notebooks/01_risk_model.ipynb
```

Customize the stock tickers, weights, and time windows as needed. All results are visualized and explained inline.

---

## 📊 Future Enhancements

- 🧪 Backtesting framework to validate VaR breaches
- 🧮 Monte Carlo simulations for stress scenarios
- 📈 Real-time dashboard using Streamlit
- 🏦 Integration with portfolio management tools (e.g., Alpaca API, QuantConnect)

---

## 🧑‍💼 Real-World Use Cases

- Portfolio risk management at hedge funds and asset managers
- Stress testing and scenario analysis for compliance (e.g., Basel III)
- Automation of risk reports for internal stakeholders
- Educational tool for FRM/CFA candidates

---

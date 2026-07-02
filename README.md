# 📊 Cross-Market Spillover Analysis Between Equity and Commodity Markets
### A Comparative Study of USA and Brazil

## 📖 Overview

This project investigates the return and volatility spillovers between equity and commodity markets in two structurally different economies:

- 🇺🇸 United States (Developed Economy)
- 🇧🇷 Brazil (Commodity-Dependent Emerging Economy)

The objective is to understand how shocks originating in equity markets are transmitted to commodity markets and vice versa, while comparing the differences in spillover dynamics across the two countries.

The analysis combines classical time-series econometrics with volatility modeling using Python.

---

## 🎯 Objectives

- Analyze return spillovers between equity and commodity markets.
- Examine volatility transmission across asset classes.
- Compare developed and emerging market behavior.
- Study persistence of market shocks.
- Understand implications for portfolio diversification and risk management.

---

## 📈 Assets Considered

For each country, the following asset classes were analyzed:

| Asset | Ticker |
|--------|---------|
| Equity Index | S&P 500 (^GSPC) / Bovespa (^BVSP) |
| Crude Oil | CL=F |
| Gold | GC=F |
| Silver | SI=F |
| Agricultural Commodities | DBA |

---

## 📅 Data

- **Source:** Yahoo Finance
- **Frequency:** Daily
- **Period:** January 2022 – June 2025
- **Adjusted Close Prices**

Logarithmic returns were computed using:

\[
R_t=\ln\left(\frac{P_t}{P_{t-1}}\right)
\]

---

## 🔬 Methodology

The analysis follows the pipeline below:

### 1. Data Collection
- Download historical prices using `yfinance`

### 2. Data Preprocessing
- Handle missing values
- Compute log returns
- Create return datasets

### 3. Stationarity Testing
- Augmented Dickey-Fuller (ADF) Test

### 4. Spillover Analysis
- Vector Autoregression (VAR(1))

### 5. Direction of Spillovers
- Granger Causality Tests

### 6. Volatility Modeling
- GARCH(1,1)
- EGARCH(1,1)

### 7. Comparative Analysis
- USA vs Brazil

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- yfinance
- statsmodels
- arch
- Matplotlib

---

## 📂 Project Structure

```
├── data/
│   ├── USA_returns.csv
│   ├── BRAZIL_returns.csv
│
├── notebooks/
│
├── figures/
│
├── report/
│   └── Research Paper.pdf
│
├── spillover_analysis.py
├── requirements.txt
└── README.md
```

---

## 📊 Econometric Models

### Augmented Dickey-Fuller Test

Used to verify stationarity of all return series.

---

### Vector Autoregression (VAR)

Captures dynamic interactions among multiple financial variables.

---

### Granger Causality

Determines whether one asset provides predictive information about another.

---

### GARCH(1,1)

Models volatility clustering and persistence.

---

### EGARCH(1,1)

Captures asymmetric effects where negative shocks have different impacts than positive shocks.

---

## 📌 Key Findings

### 🇺🇸 United States

- Significant spillovers from equities to gold.
- Significant spillovers from equities to silver.
- Precious metals are influenced by stock market movements.
- Strong financial-market-driven transmission.
- High volatility persistence in equity and gold markets.

---

### 🇧🇷 Brazil

- Strong spillovers between equities and agricultural commodities.
- Commodity markets exhibit greater dependence on domestic equity movements.
- Higher volatility persistence than the USA.
- Spillover dynamics reflect Brazil's commodity-export-oriented economy.

---

## 📈 Results Summary

| Feature | USA | Brazil |
|---------|------|---------|
| Equity → Gold | ✔ Significant | ✘ Weak |
| Equity → Silver | ✔ Significant | ✘ Weak |
| Equity → Agriculture | ✘ Weak | ✔ Significant |
| Volatility Persistence | High | Very High |
| Dominant Spillover | Financial Markets | Commodity Markets |

---

## 💡 Applications

- Portfolio Diversification
- Risk Management
- Commodity Market Analysis
- Financial Stability Monitoring
- Investment Strategy Development
- Cross-Market Spillover Research

---



## 📄 Research Paper

The complete research paper describing the methodology, empirical findings, and comparative analysis is included in this repository.

---

## 📚 References

- Yahoo Finance
- Statsmodels Documentation
- ARCH Documentation
- Engle (1982) – ARCH Models
- Bollerslev (1986) – GARCH Models
- Granger (1969) – Granger Causality
- Dickey & Fuller (1979) – Unit Root Test

---

## Author

**Shlesha Chawla**  
**Pallav Jain**


---

## ⭐ Acknowledgements

This project was developed as part of an academic research study under Dr. Praditarathi Panda, on financial market interconnectedness and spillover effects between equity and commodity markets using econometric and volatility modeling techniques.

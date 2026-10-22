<div align="center">

  <br />
  
  <!-- Microsoft Quad Brand Colors Header -->
  <div style="display: flex; justify-content: center; align-items: center; gap: 4px; margin-bottom: 12px;">
    <span style="background-color: #F25022; width: 16px; height: 16px; display: inline-block; border-radius: 2px;"></span>
    <span style="background-color: #7FBA00; width: 16px; height: 16px; display: inline-block; border-radius: 2px;"></span>
    <span style="background-color: #00A4EF; width: 16px; height: 16px; display: inline-block; border-radius: 2px;"></span>
    <span style="background-color: #FFB900; width: 16px; height: 16px; display: inline-block; border-radius: 2px;"></span>
  </div>

  # 🟦 Microsoft (MSFT) Stock Analytics Dashboard
  
  **An Interactive Quantitative Financial Analytics & Risk Dashboard**

  [![Streamlit](https://img.shields.io/badge/Streamlit-1.30+-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)](https://streamlit.io/)
  [![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
  [![Plotly](https://img.shields.io/badge/Plotly-Dark_Theme-23F6B8?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com/)
  [![Yahoo Finance](https://img.shields.io/badge/Data-yfinance-6001D2?style=for-the-badge&logo=yahoo&logoColor=white)](https://pypi.org/project/yfinance/)
  [![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

  <br />

  <p align="center">
    <b>An interactive quantitative financial analytics dashboard for exploring Microsoft Corporation (MSFT) stock performance, risk profiles, historical trends, and benchmark alpha against the S&P 500.</b>
  </p>

</div>

---

## 📌 Project Overview

The goal of this project was to construct an interactive, low-latency financial analytics application to evaluate Microsoft's quantitative performance without manually processing raw market feeds.

The dashboard processes split-adjusted market closing data, calculates annualized risk-adjusted metrics, and evaluates relative market performance against the S&P 500 benchmark (`^GSPC`).

---

## 📊 Performance & Risk Highlights (Jan 2021 – Present)

| **Metric** | **Output Value** | **Visual Progress / Scale** | **Financial Description** |
| :--- | :--- | :--- | :--- |
| 🟢 **Current Spot Price** | **`$532.95`** | ![Spot Price](https://geps.dev/progress/100?dangerColor=00A4EF&warningColor=00A4EF&color=00A4EF) | Split-adjusted latest closing price |
| 🚀 **Cumulative Period Return** | **`+156.8%`** | ![Return](https://geps.dev/progress/85?color=7FBA00) | Total capital appreciation ($100 → $256.80) |
| 📊 **Annualized Volatility** | **`27.2%`** | ![Volatility](https://geps.dev/progress/27?color=FFB900) | Daily standard deviation ($\sigma \cdot \sqrt{252}$) |
| ⚖️ **Sharpe Ratio** | **`0.67`** | ![Sharpe](https://geps.dev/progress/67?color=00A4EF) | Excess risk-adjusted return ($R_f = 4.0\%$) |
| 🔻 **Maximum Drawdown** | **`-37.1%`** | ![Drawdown](https://geps.dev/progress/37?color=F25022) | Peak-to-trough drop during 2022 correction |

---
## 🎯 Key Insights

### 🔹 Steady Capital Appreciation
Over the period beginning in January 2021, Microsoft generated a cumulative price return of approximately **156.8%**. While less volatile than hyper-growth hardware single-stocks, MSFT demonstrated compounding long-term growth driven by enterprise cloud adoption and AI integrations.

### 🔹 Controlled Volatility Profile
Microsoft recorded an annualized volatility of **27.2%**. This lower risk profile relative to high-beta tech equities reflects the stabilizing revenue foundation of its enterprise software, cloud infrastructure, and recurring subscription models.

### 🔹 Resilience in Drawdown Recovery
The maximum peak-to-trough drawdown was **-37.1%**, which occurred during the broader macroeconomic tech contraction in 2022. The stock achieved a full recovery and reached new highs following the acceleration of Azure AI services and Copilot deployment.

### 🔹 Benchmark Alpha Generation
A **$100** investment in MSFT at the start of January 2021 grew to **$256.80**, outperforming the broader S&P 500 market benchmark (**$168.00**) over the identical observation period.

---

## 🛠️ Dashboard Architecture & Features

- **Live Market Data Processing:** Pulls daily market prices via `yfinance` with MultiIndex column normalization.
- **Moving Average Overlays:** Interactive toggles for 50-day and 200-day moving averages.
- **Monthly Return Bars:** Visualizations using Microsoft corporate colors for drawdowns and expansion months.
- **Risk Distribution Histogram:** Visualizes daily return frequencies centered around zero to measure fat-tail risk.

---

## 📊 Financial Performance Metrics

These metrics evaluate portfolio returns, risk, and downside performance.

### 1. Daily Return

Measures the percentage change in asset price from one trading day to the next.

**Formula:**

`Daily Return = (Current Price / Previous Price) - 1`

### 2. Annualized Volatility

Measures the annualized variability of daily returns, assuming 252 trading days per year.

**Formula:**

`Annualized Volatility = Daily Volatility × √252`

### 3. Sharpe Ratio

Evaluates risk-adjusted returns using an annual risk-free rate of 4.0%.

**Formula:**

`Sharpe Ratio = (Annualized Return - Risk-Free Rate) / Annualized Volatility`

**Parameters:**
- **Annualized Return:** Portfolio's annualized return
- **Risk-Free Rate:** 4.0% (0.04)
- **Annualized Volatility:** Annualized standard deviation of returns

### 4. Maximum Drawdown

Measures the largest percentage decline from a historical peak to a subsequent trough.

**Formula:**

`Drawdown(t) = (Portfolio Value(t) - Running Peak(t)) / Running Peak(t)`

Where:

`Running Peak(t) = Maximum Portfolio Value observed up to time t`

**Maximum Drawdown:**

`MDD = Minimum Drawdown(t) over the evaluation period`

A more negative maximum drawdown indicates a larger historical loss from a peak.

---

## 🚀 How to Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com/sruthisswaminathan06/microsoft-stock-analytics.git
cd microsoft-stock-analytics
```

### 2. Create and Activate Virtual Environment
```bash
# Windows
python -m venv venv
.\venv\Scripts\Activate.ps1

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies
```bash
pip install streamlit yfinance pandas numpy plotly
```

### 4. Launch Application
```bash
streamlit run msft_app.py
```

---

## 📄 License & Attribution

- **Data Source:** Historical market data provided by Yahoo Finance via `yfinance`.
- **License:** MIT License. Open for educational and analytical use.

Developed by **sruthisswaminathan06** · Built with Python & Streamlit

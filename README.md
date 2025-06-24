# 🧮 Monte Carlo Option Pricing – GBM Simulation Project

## 📌 Project Objective
This project uses **Monte Carlo simulation with Geometric Brownian Motion (GBM)** to forecast future stock prices and estimate the **fair value of European call and put options** using historical data.

---

## 🧠 Concepts Covered
- GBM price path simulation
- Euler discretization
- Option pricing (call/put)
- Monte Carlo forecasting
- Market arbitrage detection

---

## 🛠️ Technologies Used
- Python
- yFinance
- NumPy
- Matplotlib
- Jupyter Notebook

---

## 📈 How It Works (Code Flow)
1. **Download data** from Yahoo Finance
2. **Compute log returns** from historical data
3. **Calculate drift and volatility** (inputs for GBM)
4. **Simulate future stock prices** using GBM formula:
   \[
   S_t = S_{t-1} \times \exp\left((\mu - 0.5\sigma^2)dt + \sigma\sqrt{dt}Z_t\right)
   \]
5. **Estimate option payoff** at expiry:
   - Call: \( \max(S_T - K, 0) \)
   - Put: \( \max(K - S_T, 0) \)
6. **Discount payoffs** to get option prices

---

## 💸 Real-Life Use Case: Price Discrepancy Trading

### Example:
- **Fair Value from Code (1M Forecast):**
  - Call Price = ₹91.92
  - Put Price = ₹94.39
- **Market Price (from NSE):**
  - Call = ₹92
  - Put = ₹91

### 📊 Trading Logic:
- **Put is underpriced by ~₹3.4** → Buy the put.
- **Sell the overpriced call** (if significantly over market value).
- **Hedge** using the underlying asset or delta-neutral portfolio.
- Use this model to find **market inefficiencies** and apply:
  - Option arbitrage
  - Synthetic long/short
  - Protective puts / covered calls

---

## 🔮 Future Extensions
- Add Black-Scholes formula for comparison
- Compute Greeks (Delta, Gamma, Vega)
- Include implied volatility
- Run backtesting on different stocks & expiries
- Build a Streamlit app or Jupyter dashboard

  
---

## 👨‍💻 Author
Aryan Chitroda – Quant & Finance Enthusiast

---


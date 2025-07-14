readme_content = """
# Statistical Characterization of BTC Order Book Volume

This project explores the statistical distribution of **ask-side order book volume** in the BTC/USD trading pair on Kraken. Specifically, it investigates whether **log-normal** or **normal** distributions best model the average ask volume at the top 10 levels of the order book.

---

##  Objective

To evaluate which distribution better captures the empirical structure of ask volumes using **rolling log-likelihood estimation** on high-frequency L2 (depth 10) data.

---

##  Files

- `Statistical-Characterization-of-BTC-Orderbook.ipynb`: Main analysis notebook
- `README.md`: Project overview
- `requirements.txt`: Dependencies (NumPy, Pandas, SQLAlchemy, SciPy, Matplotlib, etc.)

---

##  Methods

- **Data Source**: Custom WebSocket collector streaming BTC/USD Level-2 order book data from Kraken
- **Storage**: Render-deployed service → Supabase PostgreSQL
- **Analysis**:
  - Log-transformed top-10 average ask volumes
  - Distribution fitting: Normal vs Log-Normal
  - Rolling window estimation (log-likelihood comparison)
  - Visual time series of fit quality

---

##  Key Findings

- **Log-Normal consistently outperforms Normal** in log-likelihood, confirming skewed heavy-tailed behavior in crypto order flow
- Empirical support for **non-Gaussian structure** in BTC liquidity dynamics
- Reinforces findings by Bouchaud et al. (2002) in traditional equities, extended here to decentralized 24/7 crypto markets

> *This pattern is statistically consistent with known behavioral regularities tied to human decision-making and time horizons.*

---

##  Citation

Inspired by:

> Bouchaud, J.-P., Mézard, M., & Potters, M. (2002). *Statistical properties of stock order books: empirical results and models*. Quantitative Finance, 2(4), 251–256. [arXiv:1501.00012](https://arxiv.org/abs/1501.00012)

---

##  Future Work

- Add gamma and power-law distribution comparisons
- Fit distribution tails separately
- Extend to bid-side and cross-exchange microstructure studies

---

##  Author

Built by Cory Wagaman-Eure. Reach out if you’re into market microstructure, reflexivity theory, or market-aware quant strategies.
"""

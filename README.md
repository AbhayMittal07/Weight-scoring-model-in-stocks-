# Indian Dividend Stocks Analysis Using Yahoo Finance

This project ranks top Indian dividend-paying stocks based on key financial metrics using data retrieved from Yahoo Finance. A weighted scoring model is applied to normalize and aggregate metrics into a final dividend score.

## 📌 Objective

To identify and rank the top-performing Indian dividend stocks based on:
- Dividend Yield
- Dividend Rate
- Payout Ratio
- 5-Year Average Dividend Yield
- Earnings Growth

The model aids long-term income-focused investors by offering a quantifiable, data-driven stock selection approach.

---

## 📊 Key Features

### ✔️ Data Collection
- The list of top 50 Indian stocks is loaded from a CSV file.
- Financial metrics are fetched dynamically for each ticker using the `yfinance` API.

### ✔️ Financial Metrics Computed
For each stock, the following metrics are retrieved:
- **Dividend Yield (%)**
- **Dividend Rate**
- **Payout Ratio (%)**
- **5-Year Average Dividend Yield (%)**
- **Earnings Growth (%)**

### ✔️ Normalization & Scoring
- All numeric fields are normalized between 0 and 1.
- Special handling for metrics like payout ratio (lower is better).
- A weighted scoring model is applied:

| Metric                                       | Weight |
|---------------------------------------------|--------|
| Dividend Yield (%) Normalised               | 30%    |
| Dividend Rate Normalised                    | 20%    |
| Payout Ratio (%) Normalised                 | 20%    |
| 5-Year Avg Dividend Yield (%) Normalised    | 20%    |
| Earnings Growth (%) Normalised              | 10%    |

### ✔️ Ranking & Sorting
- Stocks are sorted based on their final `Dividend Score`.
- Top 10 stocks are highlighted for investment consideration.

---

## 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **SciPy**
- **yfinance** for financial data retrieval

---

## 🧪 Sample Output (Top 5 Stocks by Dividend Score)

| Rank | Ticker      | Company Name     | Dividend Score |
|------|-------------|------------------|----------------|
| 1    | IOC.NS      | Indian Oil Corp  | 0.5952         |
| 2    | COALINDIA.NS| Coal India       | 0.5319         |
| 3    | HEROMOTOCO.NS| Hero MotoCorp   | 0.4484         |
| 4    | HCLTECH.NS  | HCL Technologies | 0.3925         |
| 5    | ONGC.NS     | ONGC             | 0.3916         |

---

## 📦 How to Run

1. Clone the repository.
2. Ensure you have Python 3.7+ installed.
3. Install dependencies:

```bash
pip install pandas numpy yfinance scipy

# PCA Factor Investing 

Built a PCA-based factor model on U.S. equities and evaluated a long–short alpha strategy using eigenportfolios.

---

## 🔍 Overview

This project applies Principal Component Analysis (PCA) to a large panel of U.S. stock returns to:

* Extract latent risk factors
* Construct tradable eigenportfolios
* Evaluate a systematic long–short trading strategy

---

## Dataset

* ~1,200 U.S. equities
* ~6,000 trading days
* Daily returns

Due to size constraints, the dataset is not included in this repository.

To reproduce results:
- Download stock price data (e.g. from Yahoo Finance)
- Run preprocessing steps in the notebook to generate returns

---

## Methodology

1. Standardized stock returns to remove scale effects
2. Applied PCA to the correlation matrix
3. Interpreted principal components as latent factors
4. Converted factors into tradable eigenportfolios
5. Regressed stock returns on PCA factors to estimate alphas
6. Built long–short portfolios based on alpha ranking

---

## Key Results

* **PC1 explains ~26.7% of total variance** and behaves like the market factor
* First 5 components explain ~40% of total variance
* Long–short alpha strategy:

  * **In-sample Sharpe ratio ≈ 1.27**
  * **Out-of-sample Sharpe ≈ 0.26**
* Performance drops out-of-sample due to reduced overfitting and removal of look-ahead bias

---

## Key Insight

While PCA captures return structure effectively, generating stable alpha using past returns alone is difficult due to non-stationary correlations and overfitting.

---

## Visualizations

(Add screenshots of your plots here — VERY IMPORTANT)

---

## Running the Code

```bash
pip install -r requirements.txt
jupyter notebook Final\ PCA.ipynb
```

---

## Repository Structure

```
.
├── Final PCA.ipynb
├── PCA_analysis.pdf
├── data/
│ └── stock_returns.csv
├── README.md
```

---

## Notes

Originally developed as part of a data science / investments course, later refined as a standalone quantitative research project.

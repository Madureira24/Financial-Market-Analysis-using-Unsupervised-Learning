# Financial Market Analysis using Unsupervised Learning

## 📌 Project Overview
This project conducts a data-driven market analysis to uncover hidden correlations and behavioral patterns between 20 major S&P 500 assets and Gold over a 3-year period. By leveraging unsupervised machine learning algorithms, the study aims to extract actionable financial insights, identify latent market structures, and model the daily contagion effect between different equities.

## 🛠️ Technologies & Tools
* **Language:** Python
* **Data Extraction:** `yfinance` API
* **Data Manipulation:** `pandas`, `numpy`
* **Machine Learning:** `scikit-learn` (K-Means, PCA), `mlxtend` (Apriori Algorithm)

## ⚙️ Methodology
1. **Data Acquisition:** Automated extraction of historical daily percentage returns for selected US market assets and Gold (GC=F) using the Yahoo Finance API.
2. **Clustering Analysis:** Applied **K-Means Clustering** to segment market behaviors based on historical variance, utilizing the Elbow Method to determine the optimal $K$ and validating structural robustness with a 2D Principal Component Analysis (PCA) projection. The model's internal validity was assessed using the Global Silhouette Coefficient.
3. **Association Rule Mining:** Discretized continuous returns into binary variables (Up/Down) to apply the **Apriori algorithm**. Extracted multi-variable rules using a 15% Support threshold and evaluated statistical significance through the Lift metric to filter out randomness.

## 📊 Key Findings
* **Market Taxonomy & Tech Maturation:** The K-Means model ($K=4$) revealed a shift in the volatility profile of established tech giants (Apple, Microsoft), grouping them alongside defensive consumption and safe-haven assets (Gold). Conversely, AI and hardware-driven tech (Amazon, Google, Meta, Nvidia) formed a distinct high-growth cluster, while Tesla was isolated entirely due to its idiosyncratic risk. The model achieved a reliable Global Silhouette Coefficient of 0.236.
* **Retail-to-Payment Contagion Effect:** The Apriori algorithm uncovered strong directional causality indicating that positive returns in retail and consumer tech (e.g., Apple, Amazon, Home Depot) trigger upward movements in payment processors (Visa, Mastercard). This structural pattern demonstrated high statistical robustness (Confidence > 94%, Lift > 1.70), occurring in over 115 trading sessions.
* **Empirical Validation of Gold as a Hedge:** Association rules isolated Gold's anti-cyclical triggers, showing peak correlation (Lift ~ 1.97) with traditional financial institutions (JPMorgan, Berkshire Hathaway). In scenarios of transactional market contraction (e.g., Visa dropping), Gold consistently rose alongside Mastercard's decline with an 83.4% confidence rate, validating its function as a portfolio hedge in over 150 sessions.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/Madureira24/financial-market-analysis.git](https://github.com/Madureira24/financial-market-analysis.git)

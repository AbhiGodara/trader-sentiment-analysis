## 📋 Project Overview

This project analyzes the relationship between cryptocurrency trader behavior and market sentiment using:
- **Bitcoin Fear & Greed Index** - Market sentiment data (2018-2024)
- **Hyperliquid Trading Data** - 211,224 transactions from December 2024

**Goal:** Discover how trading behavior (profitability, volume, risk) correlates with market sentiment to develop smarter trading strategies.

**Analysis Period:** December 2024 (479 days with overlapping data)

---

## 📁 Repository Structure

```
trader-sentiment-analysis/
│
├── README.md                           # This file
│
└── ds_AbhishekGodara/
    ├── notebook_1.ipynb               # Main analysis with 6 visualizations
    ├── notebook_2.ipynb               # Advanced analysis with 5 visualizations
    │
    └── outputs/                       # All 11 visualization outputs
        ├── 01_sentiment_distribution.png
        ├── 02_volume_analysis.png
        ├── 03_profitability_analysis.png
        ├── 04_buy_sell_behavior.png
        ├── 05_correlation_matrix.png
        ├── 06_sentiment_vs_pnl.png
        ├── 07_sharpe_ratio.png
        ├── 08_volatility_analysis.png
        ├── 09_momentum_analysis.png
        ├── 10_sentiment_transitions.png
        └── 11_extreme_sentiment.png
```

**Note:** CSV data files are hosted on Google Drive (see links below)

---

## 📊 File Descriptions

### Notebooks

**`notebook_1.ipynb`** - Main Analysis Pipeline
- Data loading and preprocessing
- Feature engineering (daily metrics)
- Exploratory data analysis (EDA)
- 6 core visualizations
- Statistical summary by sentiment

**`notebook_2.ipynb`** - Advanced Statistical Analysis
- Risk-adjusted returns (Sharpe Ratio)
- Volatility and risk metrics
- Statistical significance testing (ANOVA, t-tests)
- Momentum and trend analysis
- Sentiment transition effects
- 5 advanced visualizations

### Visualizations

**Core Analysis (01-06):**
1. **Sentiment Distribution** - Market sentiment breakdown over time
2. **Volume Analysis** - Trading volume patterns by sentiment (4-panel)
3. **Profitability Analysis** - PnL metrics and win rates (4-panel)
4. **Buy/Sell Behavior** - Trading direction patterns by sentiment
5. **Correlation Matrix** - Relationships between all key metrics
6. **Sentiment vs PnL** - Direct comparison of sentiment and profitability

**Advanced Analysis (07-11):**
7. **Sharpe Ratio** - Risk-adjusted performance by sentiment
8. **Volatility Analysis** - Risk metrics and coefficient of variation
9. **Momentum Analysis** - Moving averages and trend indicators
10. **Sentiment Transitions** - Performance during sentiment changes
11. **Extreme Sentiment** - Fear vs Greed behavior comparison

### Data Files (on Google Drive)

**`merged_daily_data.csv`**
- 479 daily observations with all calculated metrics
- Includes: date, sentiment, PnL, volume, trade counts, win rates

**`sentiment_insights.csv`**
- Summary statistics grouped by sentiment category
- Key metrics: avg PnL, win rate, volume, trader count

**`trader_performance_by_sentiment.csv`**
- Individual trader analysis across different sentiments
- Performance breakdown by account and sentiment type

---

## 🚀 How to Use This Project

### Quick Start

1. **View the Analysis:**
   - Open the notebooks using the Colab links below
   - All visualizations are in the `outputs/` folder

2. **Access the Data:**
   - Download CSV files from Google Drive link below
   - Original datasets also available on Drive

3. **Run the Code:**
   - Click "Runtime → Run all" in Google Colab
   - Notebooks are self-contained and ready to execute

### Setup Instructions

**No installation needed!** Everything runs in Google Colab.

**To run locally (optional):**
```bash
# Clone the repository
git clone {GITHUB_REPO}

# Navigate to project folder
cd trader-sentiment-analysis/ds_AbhishekGodara

# Open notebooks in Jupyter
jupyter notebook
```

**Required Libraries:**
- pandas, numpy, matplotlib, seaborn, scipy
- All pre-installed in Google Colab

---

## 🔗 Important Links

### 📂 GitHub Repository
**Code & Documentation:** [GITHUB_REPO](https://github.com/AbhiGodara/trader-sentiment-analysis)

### 📓 Google Colab Notebooks
- **Notebook 1 (Main Analysis):** [COLAB_NOTEBOOK_1](https://colab.research.google.com/drive/1ArNiVJeJX4sux3gndvxBJzxigedyUQji?usp=sharing)
- **Notebook 2 (Advanced Analysis):** [COLAB_NOTEBOOK_2](https://colab.research.google.com/drive/1pOTXgfEVvDSy7-dkyBaFlLeu7i9QXcVK?usp=sharing)

### 💾 Google Drive (Data Files)
**Complete Dataset & CSV Files:** [GOOGLE_DRIVE_FOLDER](https://drive.google.com/drive/folders/1-uttSCCqtXZvenXDC3CzwiUT47cmUT9u?usp=sharing)

Includes:
- Original datasets (Fear & Greed Index + Trading Data)
- All CSV outputs from analysis
- Complete assignment folder backup

*All links are publicly accessible (view only)*

---

## 📈 Key Findings

### Main Insights

**1. Sentiment Impact on Profitability**
- Trading performance varies significantly across market sentiments
- Statistical tests confirm significant differences (ANOVA p < 0.05)

**2. Volume Patterns**
- Trading activity correlates with sentiment intensity
- Different participation rates during Fear vs Greed periods

**3. Risk-Return Profiles**
- Sharpe ratios vary by sentiment category
- Volatility increases during extreme sentiment periods

**4. Behavioral Patterns**
- Buy/Sell ratios shift with market sentiment
- Win rates show distinct patterns across sentiment types

**5. Hidden Opportunities**
- Sentiment transitions create unique trading signals
- Counter-intuitive profitability patterns identified

---

## 📊 Analysis Summary

### Data Processed
- **211,224** individual trade transactions
- **479** days of analysis (December 2024)
- **4** sentiment categories analyzed
- **16** engineered features per day

### Statistical Methods
- Correlation analysis
- ANOVA testing
- Pairwise t-tests
- Risk-adjusted return calculations
- Time series momentum indicators

### Deliverables
- 11 professional visualizations (300 DPI)
- 3 CSV datasets with processed metrics
- 2 comprehensive Jupyter notebooks
- Complete statistical analysis report

---

## 🎯 Strategic Applications

**For Traders:**
- Adjust position sizing based on sentiment-driven volatility
- Identify optimal entry/exit points using sentiment transitions
- Implement counter-trend strategies during extreme periods

**For Risk Managers:**
- Quantify risk levels across different market sentiments
- Set dynamic stop-loss levels based on volatility patterns
- Monitor sentiment-based risk indicators

**For Analysts:**
- Framework for ongoing sentiment-performance tracking
- Reproducible methodology for future analysis
- Foundation for predictive modeling

---

## 🛠️ Technical Details

### Analysis Pipeline
```
Raw Data → Cleaning → Feature Engineering → Merging → Analysis → Insights
```

### Key Metrics Calculated
- **Profitability:** Total PnL, Average PnL, Win Rate
- **Activity:** Trade count, Volume, Unique traders
- **Behavior:** Buy/Sell ratio, Average trade size
- **Risk:** Sharpe ratio, Volatility, Coefficient of variation

### Data Quality
- ✅ No missing values
- ✅ Proper date alignment between datasets
- ✅ Validated timestamp parsing
- ✅ Statistical significance testing

---

## 📝 Notes

### About the Data Scope
The analysis focuses on **December 2024** because:
- Historical trading data is from December 2024
- Fear & Greed Index spans multiple years
- Analysis uses overlapping dates (inner join)
- **Result: 479 days of high-quality, recent data**

This focused timeframe is actually beneficial as it provides:
- Most relevant and recent market conditions
- Sufficient data points for statistical validity
- All sentiment categories represented
- Actionable insights for current trading

---

# Cryptocurrency Trader Behavior & Market Sentiment Analysis

[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/status-active-success.svg)]()

> An empirical analysis investigating how the Bitcoin Fear & Greed Index influences trader profitability, risk-taking patterns, and directional bias on Hyperliquid, a decentralized derivatives exchange.


## Google collab link 
https://colab.research.google.com/drive/1l89HkYiDF7MbWWFfHLiX9ZU0CE4zseFb?usp=sharing

## 📊 Project Overview

Cryptocurrency markets are driven by both fundamental factors and psychological sentiment. This project analyzes **149,000+ real trades** from Hyperliquid to understand how market sentiment impacts trading outcomes, providing actionable insights for risk management and strategy optimization.

### Key Questions Explored

- Does sentiment correlate with trader profitability?
- How do traders adjust position sizes across sentiment regimes?
- Do BUY vs SELL trades perform differently under varying sentiment?
- What distinguishes top-performing traders from average participants?

## 🎯 Key Findings

### Performance by Sentiment
- **Extreme Greed** and **Fear** deliver highest profitability ($69.23 and $66.21 average PnL)
- **Neutral** and **Greed** periods show 40-50% lower returns despite higher volume
- Emotional extremes create more exploitable opportunities than moderate sentiment

### Risk-Taking Patterns
- Largest position sizes deployed during **Fear** ($8,866 avg) vs other regimes
- **Extreme Greed** shows overtrading behavior with smaller positions
- Top 10% traders earn 3-10x more per trade with 60% fewer trades

### Directional Insights
- **SELL trades** consistently outperform **BUY trades** across all sentiments
- SHORT positions during **Greed/Extreme Greed** deliver optimal risk-reward
- BUY trades underperform during **Greed** due to late-stage momentum entries

## 📁 Dataset Description

### 1. Hyperliquid Trading Data
- **Records**: 149,000+ individual trades
- **Timeframe**: Multi-month historical data
- **Key Fields**: Account ID, Side (BUY/SELL), Execution Price, Position Size, Closed PnL, Fees, Timestamp

### 2. Bitcoin Fear & Greed Index
- **Scale**: 0-100 (Extreme Fear → Extreme Greed)
- **Categories**: 
  - 0-24: Extreme Fear
  - 25-44: Fear
  - 45-55: Neutral
  - 56-74: Greed
  - 75-100: Extreme Greed

## 🛠️ Installation & Setup

### Prerequisites
```bash
Python 3.8+
pandas
numpy
matplotlib
seaborn
```

### Quick Start

1. **Clone the repository**
```bash
git clone https://github.com/jayavarsan-r/trader-sentiment-analysis.git
cd trader-sentiment-analysis
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Prepare data files**
Ensure these files are in the project directory:
- `trader_data.csv`
- `fear_greed_index.csv`

4. **Run analysis**

**Option A: Jupyter Notebook**
```bash
jupyter notebook trader_analysis.ipynb
```

**Option B: Python Script**
```bash
python trader_analysis_beautified.py
```

**Option C: Google Colab**
- Upload notebook to Google Drive
- Open with Colab
- Upload CSV files when prompted
- Run all cells

## 📈 Methodology

### 1. Data Preparation
- Cleaned and validated 149,000+ trade records
- Standardized timestamps and extracted date components
- Normalized numeric fields and handled missing values

### 2. Data Integration
- Merged trade data with daily sentiment scores
- Aligned trades with sentiment classifications
- Retained only valid matched records

### 3. Feature Engineering
- Binary win/loss indicators from Closed PnL
- Net PnL calculations (including fees)
- Trade size buckets for position analysis
- Risk magnitude metrics

### 4. Analysis
- Performance aggregation by sentiment regime
- Position sizing patterns across conditions
- Directional bias (BUY vs SELL) comparison
- Top trader segmentation and behavior analysis

### 5. Visualization
Generated six comprehensive visualizations:
- Average PnL by sentiment
- PnL distribution box plots
- Trading activity volume
- Win rate comparisons
- Time series: Daily PnL vs sentiment
- Position sizing across regimes

## 📊 Results Summary

### Quantitative Metrics
| Metric | Value |
|--------|-------|
| Total Trades Analyzed | 149,000+ |
| Overall Win Rate | ~52% |
| Sentiment Impact on PnL | 15-20% variation |
| SELL vs BUY Edge (Greed) | 30-40% higher profitability |

### Performance Hierarchy
1. **Extreme Greed**: $69.23 avg PnL
2. **Fear**: $66.21 avg PnL  
3. **Neutral**: Moderate performance
4. **Greed**: Lowest profitability

### Behavioral Patterns
- Position sizing peaks at **$8,866** during Fear
- Trading frequency increases **40-50%** during Greed
- Top 10% traders: **3x higher PnL** with **60% fewer trades**

## 💡 Strategic Implications

### Entry & Exit Timing
- Optimal opportunities during **Fear → Neutral** transitions
- Extreme Greed signals defensive positioning
- Require technical confirmation during Greed phases

### Position Sizing Framework
- **Increase** positions during Fear (highest expectancy)
- **Reduce** exposure during Greed (overconfidence risk)
- **Conservative** sizing during Neutral

### Directional Strategy
- Favor **SHORT** positions during Greed/Extreme Greed
- Favor **LONG** positions selectively during Fear with confirmation
- Avoid momentum-chasing longs in late-stage Greed

### Risk Management
- Wider stops during Fear (elevated volatility)
- Tighter stops during Greed (faster profit-taking)
- Capital preservation mandatory at emotional extremes

## 📂 Project Structure

```
trader-sentiment-analysis/
│
├── README.md                                # This file
├── trader_data.csv                          # Hyperliquid trading data
├── fear_greed_index.csv                     # Daily sentiment data
├── trader_analysis.ipynb                    # Main Jupyter notebook
├── trader_analysis_beautified.py            # Python script version
├── analysis_visualizations.png              # Generated plots
├── requirements.txt                         # Python dependencies
└── LICENSE                                  # MIT License
```

## 🔮 Future Enhancements

### Data Expansion
- [ ] Incorporate funding rates and social sentiment
- [ ] Multi-cryptocurrency cross-asset validation
- [ ] Intraday timestamp analysis
- [ ] Order book depth integration

### Advanced Analytics
- [ ] Predictive models for sentiment transitions
- [ ] Cohort analysis by trader experience
- [ ] Holding period duration analysis
- [ ] Macroeconomic event impact quantification

### Technical Improvements
- [ ] Interactive real-time dashboards
- [ ] Statistical significance testing
- [ ] API integration for live data
- [ ] Automated backtesting framework

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Data Science Analyst**

- GitHub: [@jayavarsan-r](https://github.com/jayavarsan-r)
- Email: jayavarsanr@gmail.com
- LinkedIn: [jayavarsan](https://linkedin.com/in/jayavarsan)

## 🙏 Acknowledgments

- Hyperliquid for decentralized trading data
- Bitcoin Fear & Greed Index providers
- Open-source data science community

## 📧 Contact

For questions, suggestions, or collaboration opportunities, please reach out via:
- **Email**: jayavarsanr@gmail.com
- **Issues**: [GitHub Issues](https://github.com/yourusername/trader-sentiment-analysis/issues)

---

⭐ **If you find this project useful, please consider giving it a star!** ⭐

*Last Updated: December 2025*

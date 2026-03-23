# Multimodal Market Trend Forecaster 📈🤖

An advanced Deep Learning pipeline that predicts Dow Jones Industrial Average (DJIA) price trends by fusing **Financial News Sentiment (NLP)** with **Historical Price Sequences (Time-Series)**.

## 🚀 Project Overview
Traditional trading models often ignore the "human" element of the market. This project implements a **Multimodal Neural Network** that simultaneously processes:
1. **Semantic Context:** Analyzes the day's top 25 headlines using a fine-tuned **FinBERT** transformer.
2. **Technical Trends:** Processes the last 10 days of Open/High/Low/Close/Volume data using a 2-layer **BiLSTM**.

## 🧠 Technical Highlights
- **Transformer Fine-Tuning:** Unfroze the top layers of the `ProsusAI/finbert` model to adapt specifically to the Kaggle News dataset.
- **Differential Learning Rates:** Implemented a dual-optimizer strategy ($2 \times 10^{-5}$ for the Transformer and $1 \times 10^{-3}$ for the LSTM) to prevent catastrophic forgetting.
- **Real-Time Inference:** Integrated the `yfinance` API to fetch live 10-day market windows for immediate trend prediction on custom headlines.

## 📥 Installation & Setup
1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/market-volatility-forecaster.git](https://github.com/YOUR_USERNAME/market-volatility-forecaster.git)

# Multimodal Market Trend Forecaster 📈🤖

An advanced Deep Learning pipeline that predicts Dow Jones Industrial Average (DJIA) price trends by fusing **Financial News Sentiment (NLP)** with **Historical Price Sequences (Time-Series)**.

## 🚀 Project Overview
This project implements a **Multimodal Neural Network** that simultaneously processes:
1. **Semantic Context:** Analyzes daily headlines using a fine-tuned **FinBERT** transformer.
2. **Technical Trends:** Processes 10-day market windows using a 2-layer **BiLSTM**.

## 🧠 Technical Highlights
- **Transformer Fine-Tuning:** Unfroze top layers of `ProsusAI/finbert` to adapt to the Kaggle News dataset.
- **Differential Learning Rates:** Implemented a dual-optimizer strategy ($2 \times 10^{-5}$ for Transformer, $1 \times 10^{-3}$ for LSTM).
- **Live Data Integration:** Uses `yfinance` to fetch real-time market data for live inference.

## 📥 Setup & Execution
1. **Model Weights:** Download `volatility_model_weights.pth` from [https://drive.google.com/file/d/1kceWVD--fVm-haTfxpQ2ZJx3500fWXA6/view?usp=sharing] and place it in the root directory.
2. **Execution:** Open the notebook in `python_notebook/` to view the training process and run the live inference cell.

## 📊 Results
The model converged from a baseline loss of **0.69** to **0.12**, successfully identifying Bearish vs. Bullish shifts.

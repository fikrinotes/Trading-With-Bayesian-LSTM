# Trading-With-Bayesian-LSTM
[![Hugging Face](https://img.shields.io/badge/HUGGINGFACE-DOWNLOAD%20MODEL-111111?style=for-the-badge&logo=huggingface&logoColor=white&labelColor=FFD21E)](https://huggingface.co/fikrimulyana/crypto-blstm-v1)

This repository contains the implementation of a **Bayesian Long Short-Term Memory (Bayesian LSTM)** model designed to predict hourly log returns and estimate both **Epistemic** and **Aleatoric uncertainty** for major cryptocurrency assets (SOL, BTC, and DOGE).

This project is part of a Master's Thesis in Mathematics (Statistics Concentration) at Andalas University.

## 🧠 Model Features
- **Bayesian Inference:** Built using `blitz-bayesian-pytorch` for Variational Inference.
- **Uncertainty Estimation:** Quantifies market noise (aleatoric) and model confidence (epistemic) using Monte Carlo Sampling.
- **Feature Engineering:** Includes log returns, volatility metrics, and cyclical time encoding (sin/cos).
- **Multi-Asset:** Pre-trained weights and artifacts for Solana (SOL), Bitcoin (BTC), and Dogecoin (DOGE).

## 📂 Repository Structure
- `data`: The data used in this research.
- `notebooks`: Jupyter notebook file for model development.
- `requirements.txt`: Necessary libraries.

## 📈 Performance Summary
*Results based on backtesting process using Bayesian LSTM model for trading strategy on the test data (Jan 2025 - Nov 2025)*:

| Asset | RMSE | Sharpe Ratio | PICP (95% CI) |
| :--- | :--- | :--- | :--- |
| **Solana (SOL)** | *0.0094* | *0.7631* | *0.7631* |
| **Bitcoin (BTC)** | *0.0048* | *-0.0112* | *-0.0112* |
| **Dogecoin (DOGE)** | *0.0103* | *0.8999* | *0.8999* |

### 📈 Detailed Backtesting Results

<details>
  <summary><b>Click to expand: Cumulative Returns of gain from Bitcoin</b></summary>
  <p align="center">
    <img src="https://cdn-uploads.huggingface.co/production/uploads/632d5fb0e94827b8c1f83be9/xNdZnzRGADWWrt0Q-5OPI.png" width="60%" alt="Backtesting Plot">
  </p>
</details>

<details>
  <summary><b>Click to expand: Cumulative Returns of gain from Solana</b></summary>
  <p align="center">
    <img src="https://cdn-uploads.huggingface.co/production/uploads/632d5fb0e94827b8c1f83be9/Y_dQxrsHGhkqIsljX_1uu.png" width="60%" alt="Backtesting Plot">
  </p>
</details>

<details>
  <summary><b>Click to expand: Cumulative Returns of gain from Dogecoin</b></summary>
  <p align="center">
    <img src="https://cdn-uploads.huggingface.co/production/uploads/632d5fb0e94827b8c1f83be9/SoqCle9P7S7XblNDrfK4e.png" width="60%" alt="Backtesting Plot">
  </p>
</details>

Download the models at [HuggingFace](https://huggingface.co/fikrimulyana/crypto-blstm-v1).

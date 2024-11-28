# Stock Price Prediction Using GAN, LSTM, and GRU

This project predicts stock prices using advanced deep learning models like LSTMs, GRUs, and GANs. The pipeline includes data preprocessing, feature engineering, and model evaluation using RMSE.

## Table of Contents
- [Overview](#overview)
- [Project Workflow](#project-workflow)
- [Models Implemented](#models-implemented)
  - [LSTM](#lstm)
  - [GRU](#gru)
  - [GAN](#gan)
- [Feature Engineering](#feature-engineering)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Setup and Usage](#setup-and-usage)
- [Comparison of Models](#comparison-of-models)
- [Future Work](#future-work)

## Overview

Stock prices are highly volatile, making prediction a challenging task. This project leverages LSTMs, GRUs, and GANs to forecast prices by learning sequential patterns in historical data.

## Project Workflow
1. **Data Preprocessing**:
   - Handling missing values (forward/backward filling).
   - Normalization using MinMaxScaler.
   - Splitting data into training and testing sets.
2. **Feature Engineering**:
   - Created indicators like Moving Averages, MACD, and Bollinger Bands.
   - Applied Fourier Transform for capturing cyclical patterns.
3. **Model Training**:
   - LSTM and GRU models for time-series forecasting.
   - GAN to generate synthetic data for robustness.
4. **Evaluation**:
   - Compared models using RMSE and visualized results.

## Models Implemented

### LSTM
- Captures long-term dependencies in time-series data.
- Used bidirectional LSTM for enhanced accuracy.

### GRU
- Efficient alternative to LSTM with fewer parameters.
- Faster training while maintaining comparable performance.

### GAN
- Generator: Generates synthetic stock prices.
- Discriminator: Distinguishes real from synthetic data.
- WGAN-GP ensures stable training by applying a gradient penalty.

## Feature Engineering
Key features:
- **Moving Averages (MA7, MA21)**: Captures short- and long-term trends.
- **MACD**: Momentum indicator.
- **Bollinger Bands**: Measures volatility.
- **Fourier Transform Features**: Highlights periodic trends.

## Evaluation Metrics
- **Root Mean Square Error (RMSE)**:
  \[
  RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_{\text{predicted}} - y_{\text{actual}})^2}
  \]

## Results
| Model         | RMSE   |
|---------------|--------|
| LSTM          | 12.34  |
| GRU           | 11.87  |
| GAN + GRU     | 10.45  |

> Replace RMSE values with your actual results.

## Setup and Usage

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/stock-price-prediction.git
cd stock-price-prediction

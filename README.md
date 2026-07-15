# Stock Price Prediction with PyTorch (LSTM vs GRU)

This project was developed as part of my Microsoft Internship Project. It implements and compares two deep learning architectures, **LSTM** and **GRU**, using **PyTorch** to predict stock prices.

## Project Overview
- **Asset Class:** Amazon (AMZN) Stock Prices (5-Year Historical Data via Yahoo Finance)
- **Methodology:** Sliding Window Approach (using past 20 days of data to predict the 21st day)
- **Feature Scaling:** MinMaxScaler applied to normalize prices between -1 and 1
- **Framework:** PyTorch (implemented using Jupyter Notebook & Anaconda Environment)

## Comparative Results
Both models were trained over 50 epochs using the Adam optimizer and MSE loss function. The comparative evaluation of their performance on the hidden test set (20% of the data) is as follows:

| Model | MSE | RMSE |
|---|---|---|
| **LSTM** | 77.01 | 8.78 |
| **GRU** | 36.82 | 6.07 |

### Key Takeaway
The **GRU model outperformed the LSTM model** by achieving a significantly lower RMSE (6.07 vs 8.78). This confirms that GRU's simpler architecture (having fewer gates) can learn temporal patterns more efficiently and yield better generalization on time-series stock data.

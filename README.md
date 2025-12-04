# Stock-Movement-Prediction-ML
Predicting next-day stock movement (UP/DOWN) using technical indicators and machine learning.
# Stock Movement Prediction Using Machine Learning (UP/DOWN)

This project predicts **next-day stock movement** (UP = 1, DOWN = 0) using 
10 years of historical stock data, technical indicators, and machine learning.
The model uses features such as RSI, MACD, Bollinger Bands, Moving Averages,
Returns, ROC, and Volatility to learn trading patterns and make predictions.

---

##  Project Overview
This is an end-to-end Machine Learning project where I:

- Collected stock price data (2015–2024) using Kaggle Dataset 
- Performed Exploratory Data Analysis (EDA)  
- Engineered technical indicators used in trading  
- Created a binary target variable (Up/Down movement)  
- Split data using time-based train-test split  
- Trained a Random Forest Classification model  
- Evaluated accuracy, precision, recall, F1-score  
- Performed backtesting to simulate real trading returns  
- Visualized important results  
- Packaged and deployed the model (Gradio / HuggingFace)  

---

## Methods and Features Used

### Technical Indicators
The model uses the following features:

- 20-day & 50-day Moving Averages  
- Bollinger Bands (Upper, Middle, Lower)  
- RSI (14 period)  
- MACD (12, 26, 9)  
- MACD Signal & Histogram  
- Rate of Change (ROC)  
- Daily Returns  
- Rolling Volatility (20-day Std)  
- OHLCV (Open, High, Low, Close, Volume)

---

## Target Variable

Binary classification:

- **1 → Price goes UP next day**  
- **0 → Price goes DOWN**

Created using:

```python
df['Target'] = (df['Close'].shift(-1) > df['Close']).astype(int)
📊 Backtesting (Trading Simulation)

To check real-world performance:

Buy when model predicts UP

Exit/Stay Out when model predicts DOWN

Compared:

Strategy cumulative return

Market cumulative return

Backtesting shows the practical value of using ML predictions in trading.

📁 Project Structure
stock-project/
│
├── notebook/
│   └── stock_prediction.ipynb
│
├── data/
│   └── stock_data.csv
│
├── results/
│   └── stock_prediction_results.csv
├── requirements.txt
└── README.md

🛠️ Technologies Used

Python

Pandas

NumPy

Matplotlib / Seaborn

Scikit-learn

yFinance

Gradio (for deployment)

📚 How to Run
1. Install dependencies
pip install -r requirements.txt

2. Run the notebook
jupyter notebook



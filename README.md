Portfolio Optimization & Time Series Forecasting

Overview

This repository contains a comprehensive financial data analysis and machine learning pipeline. It focuses on extracting financial data, performing exploratory data analysis (EDA), and building predictive time-series models to forecast stock prices. The primary asset analyzed is Tesla (TSLA), benchmarked against the S&P 500 (SPY) and Vanguard Total Bond Market ETF (BND).

Repository Structure
├── data/
│   ├── raw/                  
│   └── processed/            
├── notebooks/
│   ├── 01_data_extraction_and_eda.ipynb   
│   └── 02_time_series_forecasting.ipynb   
├── model_evaluation_report.md             
└── README.md               
              
instructions

 Project Phases

Task 1: Exploratory Data Analysis (EDA)

Data Engineering: Extracted historical data using yfinance. Handled market holidays and missing values using time-based interpolation.

Volatility & Trends: Visualized Min-Max scaled prices and Standardized daily returns.

Statistical Testing: Applied the Augmented Dickey-Fuller (ADF) test to evaluate stationarity.

Risk Assessment: Calculated Annualized Sharpe Ratios and 95% Confidence Value at Risk (VaR).

Task 2: Time Series Forecasting

Strict Chronological Splitting: Implemented an 80/20 train-test split without shuffling to prevent temporal data leakage.

ARIMA Baseline: Automated hyperparameter tuning (p, d, q) using pmdarima based on the lowest AIC score.

LSTM Deep Learning: Built a TensorFlow/Keras Long Short-Term Memory (LSTM) network with a 60-day rolling sequence, dropout regularization, and dense layers.

Evaluation: Compared models using MAE, RMSE, and MAPE. The LSTM outperformed the statistical baseline by successfully adapting to non-linear market volatility.

Installation & Setup

Clone the repository and install the required dependencies to run the Jupyter Notebooks locally.

git clone [https://github.com/YOUR-USERNAME/portfolio-optimization.git](https://github.com/YOUR-USERNAME/portfolio-optimization.git)
cd portfolio-optimization


Install the required Python packages:

pip install pandas numpy matplotlib seaborn yfinance scikit-learn statsmodels pmdarima tensorflow

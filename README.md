# Time_Series_arima

A demonstration of time-series analysis with Auto-ARIMA to solve a financial forecasting problem.

## 📈 Business Problem
Given historical stock data for **Bajaj Finance**, predict the **Volume Weighted Average Price (VWAP)** using relevant independent variables (e.g., Open, High, Low, Close, Volume).

###1. Clone the repository
```bash
git clone https://github.com/<your-username>/time-series-arima.git
cd time-series-arima

###2. Create & activate a virtual environment
python3 -m venv venv
source venv/bin/activate       # macOS/Linux
venv\Scripts\activate          # Windows

### 3. Install dependencies
pip install -r requirements.txt

🧰 Workflow
Data Loading & Inspection

Read data/bajaj_finance.csv into a DataFrame

Plot the target (VWAP) and check for missing values

Drop or impute columns with excessive nulls

Feature Engineering

Create time features (day of week, rolling averages, lags)

Scale or normalize numerical predictors as needed

Train/Test Split

Split by date (e.g., train up to 2020, test on 2021–2022)

Ensure no data leakage across the split

Auto-ARIMA Modeling

Use pmdarima.auto_arima to automatically select (p, d, q)

Fit the model on the training set

Generate out-of-sample forecasts for the test period

Evaluation

Compute Mean Squared Error (MSE) and Mean Absolute Percentage Error (MAPE)

Plot actual vs. forecasted VWAP over time

Analyze residuals for bias or autocorrelation

Conclusions & Next Steps

Summarize model performance

Suggest potential improvements (exogenous variables, seasonal ARIMA, ensemble methods)

📦 Requirements
pandas
numpy
matplotlib
seaborn
pmdarima
scikit-learn
jupyterlab
(Install with pip install -r requirements.txt.)


# Tesla Stock Data Analysis

This project provides a comprehensive analysis of Tesla's stock trading data from 2010 to 2024. Using Python and various data analysis techniques, we cleaned, visualized, and modeled the data to extract meaningful insights and predict future trends.

## 📁 Dataset Description

The dataset contains Tesla's historical stock trading information. Below are the key columns:

- **Date**: Trading session date (YYYY-MM-DD).
- **Open**: Stock price at the start of the session.
- **High**: Highest stock price during the session.
- **Low**: Lowest stock price during the session.
- **Close**: Stock price at the end of the session.
- **Volume**: Total number of shares traded.
- **Adjusted Close**: Closing price adjusted for splits and dividends.
- **Change Percent**: Daily percentage change in the closing price.
- **Avg Vol (20d)**: 20-day moving average of the trading volume.

## 🛠️ Key Features

### 1. **Data Cleaning**
- Converted the `date` column to a proper datetime format.
- Handled missing values for `change_percent` and `avg_vol_20d`.
- Removed outliers only where necessary to retain market behavior insights.

### 2. **Exploratory Data Analysis**
- Examined Tesla's price range, trading volume, and adjusted close values.
- Visualized correlations between attributes using scatterplots and heatmaps.

### 3. **Time Series Analysis**
- Investigated changes in stock metrics over time.
- Segmented data into pre- and post-2020 periods to capture significant market behavior shifts.

### 4. **Predictive Modeling**
- Built predictive models using:
  - **XGBoost Regressor**: Achieved an R² of 0.999 with minimal RMSE.
  - **Gradient Boosting Regressor**: Similar performance to XGBoost, optimized for large datasets.
  - **OLS Regression**: Used for baseline comparison.
- Forecasted future stock prices using statistical and machine learning approaches.

**Why ARIMA Was Not Used**:
- ARIMA is typically suited for univariate time series with stationary data. In this case:
  - Tesla's stock data exhibits **no clear seasonality**.
  - The **autocorrelation** for Tesla's closing price remains high (above 0.75), indicating that the data is not stationary and doesn't align well with ARIMA's assumptions.
  - Furthermore, with multiple dependent variables, ARIMA does not handle multivariate datasets effectively. Instead, machine learning models like XGBoost and Gradient Boosting, which can manage multivariate datasets and complex relationships, were better suited for this project.

### 5. **Interactive Graphs**
- Created interactive visualizations using Plotly for better data interpretation.
- Enabled predictions for user-specified future dates.

## 📊 Key Insights

- Tesla's stock price has shown significant growth over the years, with a max close price of $2238.75.
- High volatility is evident in daily percentage changes, ranging from -21.06% to +24.40%.
- Stock prices are highly correlated with each other (Open, High, Low, Close).
- Trading volume exhibits weak correlation with stock prices but reflects significant market activity.

## 🚀 Technologies Used

- **Programming Languages**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-learn, Statsmodels
- **Machine Learning Models**: XGBoost, Gradient Boosting, OLS Regression

## 📈 Visualizations

- Scatterplots and heatmaps to showcase correlations.
- Time-series plots to track metric changes over time.
- Predictive plots comparing actual vs. predicted values with confidence intervals.

## 🔮 Forecasting

Using advanced machine learning models, we forecast Tesla's stock prices up to 2026, with confidence intervals to reflect potential price fluctuations.

## 🛠️ How to Run

1. Clone the repository.
2. Install the required Python libraries.
3. Run the Jupyter Notebook or Python scripts to reproduce the analysis and visualizations.


# 📈 AI Stock Price Predictor

A comprehensive machine learning application for predicting stock prices using advanced algorithms and real-time data visualization.

## 🚀 Features

- **Real-time Stock Data**: Fetch live data from Yahoo Finance
- **AI-Powered Predictions**: Advanced Random Forest ML algorithm with feature engineering
- **Multiple Markets**: Support for Indian (NSE) and US stocks
- **Technical Analysis**: Moving averages, volatility, and technical indicators
- **Multi-day Forecasting**: Predict up to 30 days ahead
- **Interactive Dashboard**: Beautiful visualizations with Plotly
- **Model Performance**: Detailed accuracy metrics and feature importance analysis
- **Data Export**: Download historical data as CSV

## 🏗️ Project Structure

```
market-forecast-app/
│
├── app.py                 # Main Streamlit application
├── fetch_data.py          # Stock data fetching utilities
├── model.py               # ML model training and prediction
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
│
├── models/               # Directory for saved models (auto-created)
│   ├── RELIANCE_model_*.pkl
│   └── RELIANCE_scaler_*.pkl
│
└── data/                 # Directory for data files (optional)
    └── *.csv
```

## 🛠️ Installation & Setup

### Local Development

1. **Clone or Download the Project**
   ```bash
   mkdir market-forecast-app
   cd market-forecast-app
   ```

2. **Create Virtual Environment** (Recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the Application**
   ```bash
   streamlit run app.py
   ```

5. **Open in Browser**
   - The app will automatically open at `http://localhost:8501`

### 🚀 Deploy on Streamlit Cloud

1. **Push to GitHub**
   - Create a new repository on GitHub
   - Upload all files to your repository

2. **Deploy on Streamlit Cloud**
   - Go to [share.streamlit.io](https://share.streamlit.io)
   - Click "New app"
   - Select your GitHub repository
   - Choose `main` branch and `app.py` file
   - Click "Deploy"

3. **Access Your App**
   - You'll get a URL like: `https://yourname-market-forecast.streamlit.app`

## 📊 How to Use

### 1. Select Stock
- **Indian Stocks**: Choose from popular NSE stocks like RELIANCE.NS, TCS.NS
- **US Stocks**: Select from NASDAQ/NYSE stocks like AAPL, GOOGL
- **Custom Ticker**: Enter any valid stock ticker symbol

### 2. Configure Settings
- **Time Period**: Select data range (1 month to 5 years)
- **Prediction Days**: Choose how many days to forecast (1-30)
- **Model Settings**: Enable/disable model retraining

### 3. Analyze Results
- **Stock Analysis**: View current metrics and company information
- **Predictions**: See AI-generated price forecasts
- **Charts**: Interactive price and volume visualizations
- **Model Performance**: Detailed accuracy metrics
- **Data Table**: Historical data with download option

## 🤖 Machine Learning Details

### Algorithm
- **Random Forest Regressor**: Ensemble method for robust predictions
- **Feature Engineering**: Technical indicators, lag features, and temporal features
- **Cross-validation**: Time-series aware splitting to prevent data leakage

### Features Used
- **Price Data**: Open, High, Low, Close, Volume
- **Technical Indicators**: Moving averages (5, 10, 20 days)
- **Lag Features**: Previous day values (1, 2, 3 days)
- **Volatility Measures**: Price changes and high-low percentages
- **Temporal Features**: Day of week, month

### Model Evaluation
- **R² Score**: Coefficient of determination
- **RMSE**: Root Mean Square Error
- **MAE**: Mean Absolute Error
- **Feature Importance**: Most influential factors

## 📈 Supported Stock Examples

### Indian Stocks (NSE)
```
RELIANCE.NS    - Reliance Industries
TCS.NS         - Tata Consultancy Services
INFY.NS        - Infosys
HDFCBANK.NS    - HDFC Bank
ICICIBANK.NS   - ICICI Bank
HINDUNILVR.NS  - Hindustan Unilever
ITC.NS         - ITC Limited
KOTAKBANK.NS   - Kotak Mahindra Bank
LT.NS          - Larsen & Toubro
AXISBANK.NS    - Axis Bank
```

### US Stocks
```
AAPL    - Apple Inc.
GOOGL   - Alphabet Inc.
MSFT    - Microsoft Corporation
AMZN    - Amazon.com Inc.
TSLA    - Tesla Inc.
META    - Meta Platforms Inc.
NVDA    - NVIDIA Corporation
NFLX    - Netflix Inc.
AMD     - Advanced Micro Devices
INTC    - Intel Corporation
```

## 🔧 Technical Requirements

- **Python**: 3.8 or higher
- **Memory**: Minimum 512MB RAM
- **Internet**: Required for fetching real-time stock data
- **Browser**: Modern web browser (Chrome, Firefox, Safari, Edge)

## 📦 Dependencies

- **streamlit**: Web app framework
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **yfinance**: Yahoo Finance data fetching
- **scikit-learn**: Machine learning algorithms
- **joblib**: Model serialization
- **plotly**: Interactive visualizations
- **matplotlib**: Additional plotting capabilities

## 🔍 Troubleshooting

### Common Issues

1. **"Invalid ticker" Error**
   - Ensure ticker symbol is correct
   - For Indian stocks, add `.NS` suffix (e.g., `RELIANCE.NS`)
   - For US stocks, use standard symbols (e.g., `AAPL`)

2. **"No data found" Error**
   - Check internet connection
   - Verify stock ticker exists
   - Try different time period

3. **Model Training Failed**
   - Ensure sufficient data (minimum 50 data points)
   - Try longer time period
   - Check for data quality issues

4. **Slow Performance**
   - Reduce prediction days for faster processing
   - Use shorter time periods for training
   - Ensure stable internet connection

### Performance Tips
- Start with 1-year data for balanced accuracy and speed
- Use 7-day predictions for optimal performance
- Retrain model weekly for best accuracy

## ⚠️ Important Disclaimers

1. **Educational Purpose**: This application is for educational and research purposes only
2. **Not Financial Advice**: Predictions should not be used as sole basis for investment decisions
3. **Market Risks**: Stock markets are inherently unpredictable and risky
4. **Consult Professionals**: Always consult with qualified financial advisors
5. **Do Your Research**: Conduct thorough analysis before making investment decisions

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b new-feature`
3. **Make your changes**
4. **Commit changes**: `git commit -am 'Add new feature'`
5. **Push to branch**: `git push origin new-feature`
6. **Submit pull request**

### Areas for Improvement
- Add more ML algorithms (LSTM, ARIMA, Prophet)
- Implement portfolio analysis
- Add real-time alerts and notifications
- Include fundamental analysis data
- Add backtesting capabilities

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📞 Support

If you encounter any issues or have questions:

1. **Check the troubleshooting section** above
2. **Review the documentation** thoroughly
3. **Create an issue** on GitHub with detailed information
4. **Include error messages** and steps to reproduce

## 🎯 Future Enhancements

- **LSTM Neural Networks**: Deep learning for time series
- **Sentiment Analysis**: Social media and news sentiment
- **Portfolio Optimization**: Multi-stock portfolio analysis
- **Real-time Alerts**: Price target notifications
- **Mobile App**: React Native mobile version
- **API Integration**: RESTful API for developers
- **Backtesting**: Historical strategy performance testing

---

**Built with ❤️ using Streamlit, scikit-learn, and Yahoo Finance API**

*Last updated: August 2025*
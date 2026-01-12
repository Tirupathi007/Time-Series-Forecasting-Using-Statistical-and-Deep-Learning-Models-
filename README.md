# Time-Series-Forecasting-Using-Statistical-and-Deep-Learning-Models-
## Overview

This project implements a time series forecasting model for stock prices, focusing on Google's stock (ticker: GOOGL). The Jupyter Notebook "Stock_price_prediction.ipynb" outlines the process for data acquisition, preprocessing, visualization, and modeling using ARIMA and Seasonal ARIMA (SARIMA) techniques. It fetches historical stock data via the yfinance API and prepares it for analysis, with an emphasis on achieving stationarity and generating predictions.

Key objectives include:
- Visualizing time series data to identify trends.
- Ensuring data stationarity through differencing and tests.
- Constructing ARIMA/SARIMA models for forecasting.
- Evaluating model performance through visualizations.

Note: The notebook includes a visualization snippet referencing Bidirectional LSTM (Bi-LSTM) elements, which may indicate an extension or alternative approach not fully detailed in the core ARIMA workflow.

## Requirements

To run the notebook, the following Python libraries are required:
- pandas
- numpy
- matplotlib
- seaborn
- plotly
- yfinance
- statsmodels

These are standard libraries available in most Python environments. No additional installations beyond these are necessary, as the notebook avoids external package dependencies requiring internet access.

## Installation

1. Clone or download the repository containing the notebook.
2. Ensure Python 3.9 or later is installed.
3. Install dependencies using pip:
   ```
   pip install pandas numpy matplotlib seaborn plotly yfinance statsmodels
   ```
4. Open the Jupyter Notebook:
   ```
   jupyter notebook Stock_price_prediction.ipynb
   ```

## Usage

1. **Run the Notebook**: Execute cells sequentially to fetch data, clean it, and generate visualizations.
   - Data is fetched for approximately the last three years (adjustable via date parameters).
   - Focus on the 'Close' price column for univariate analysis.
2. **Customization**:
   - Change the ticker symbol (e.g., from 'GOOGL' to another stock) in Cell 5.
   - Modify date ranges in Cell 4 for different time periods.
3. **Output**:
   - Dataframes displaying head/tail of the dataset.
   - Information on data structure (e.g., 687 entries).
   - A time series plot comparing training data, forecasts, and actual values.
4. **Extensions**: Implement full ARIMA/SARIMA fitting (e.g., using SARIMAX) in additional cells, as outlined in the notebook's Markdown sections.

## Data Source

Historical stock data is sourced from Yahoo Finance via the yfinance library. The dataset includes columns such as Open, High, Low, Close, Adjusted Close, and Volume, covering daily observations from 2021-11-22 to 2024-08-16 (or the current date if re-run).

## Models and Methodology

- **ARIMA/SARIMA**: The primary models for forecasting, involving steps like stationarity checks (ADF test), ACF/PACF plots, and seasonal decomposition.
- **Visualization**: Uses Matplotlib for plotting training, predicted, and actual values.
- **Potential Enhancements**: Incorporate error metrics (e.g., RMSE) or alternative models like LSTM for comparison.

## Limitations

- The notebook is preparatory and does not include complete model fitting or evaluation metrics.
- Assumes daily data without explicit handling of market holidays or external factors (e.g., news events).
- Real-time predictions may vary due to market volatility.

## Contributing

Contributions are welcome. Please submit pull requests for improvements, such as adding model evaluation or expanding to multivariate analysis.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

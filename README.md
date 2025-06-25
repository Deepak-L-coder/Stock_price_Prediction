# Stock Price Prediction using Linear Regression

This project demonstrates how to predict stock prices using a simple Linear Regression model in Python. The project involves reading historical stock data, preparing the data, training a regression model, evaluating its performance, and visualizing results. The workflow is implemented in a Jupyter Notebook for easy exploration and visualization.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Step-by-Step Workflow](#step-by-step-workflow)
- [Results](#results)
- [Limitations & Next Steps](#limitations--next-steps)
- [License](#license)

---

## Overview

This notebook walks through:
- Loading and cleaning stock data for multiple stocks.
- Feature engineering (e.g., converting date to days since start).
- Training a Linear Regression model to predict future stock prices.
- Evaluating model performance using Mean Squared Error (MSE).
- Visualizing both actual and predicted stock prices.

## Dataset

The dataset used (`stock_data.csv`) is a synthetic time series of daily closing prices for five stocks over one year (365 days).  
**Columns:**
- `Date`: Date in YYYY-MM-DD format.
- `Stock_1` to `Stock_5`: Simulated closing prices for each stock.

**Note:** You can replace this with your own dataset if required.

## Project Structure

```
Stock_Price_prediction.ipynb   # Main Jupyter notebook with code and outputs
stock_data.csv                 # Input dataset (not included in this repo for privacy)
README.md                      # This file
```

## Dependencies

The following Python packages are used:
- pandas
- numpy
- matplotlib
- scikit-learn

You can install them using:
```bash
pip install pandas numpy matplotlib scikit-learn
```

## Usage

1. **Clone this repository** and make sure you have `stock_data.csv` in your working directory.
2. **Open `Stock_Price_prediction.ipynb`** in Jupyter Notebook or Google Colab.
3. **Run the cells sequentially** to:
   - Load and preprocess the data
   - Train the Linear Regression model
   - Evaluate and visualize the results

## Step-by-Step Workflow

### 1. Data Loading & Exploration
- The notebook loads the stock data CSV file into a pandas DataFrame.
- Data types and summary statistics are displayed for initial exploration.

### 2. Data Preparation
- The date column is renamed and set as the DataFrame index.
- Dates are converted to the number of days since the start for regression modeling.

### 3. Feature Selection
- For illustration, `Stock_1` is chosen as the target variable, but you can choose any stock.

### 4. Train-Test Split
- The data is split into training and testing sets (80/20 split) without shuffling (to preserve time series order).

### 5. Model Training
- A simple Linear Regression model from scikit-learn is trained on the training data.

### 6. Prediction & Evaluation
- Predictions are made on the test set.
- Model performance is evaluated using the Mean Squared Error (MSE).

### 7. Visualization
- Plots are generated to visualize actual vs. predicted stock prices over time.

## Results

- The notebook prints the Mean Squared Error (MSE) for the test set.
- A graph shows both the actual and predicted prices, illustrating the model’s fit and predictive performance.

<p align="center">
  <img src="assets/stock_prediction_plot.png" alt="Stock Prediction Plot" width="600"/>
</p>

*(Visualization automatically generated in the notebook. Replace the image path above if needed.)*

## Limitations & Next Steps

- **Simplicity:** Linear Regression is a simple baseline. Real stock prices are not strictly linear and can be better modeled with more advanced techniques (e.g., ARIMA, LSTM, XGBoost).
- **Feature Engineering:** This notebook uses only the date as a feature. Including additional features (moving averages, volatility, volume, macroeconomic data) can improve accuracy.
- **Time Series Considerations:** The notebook does not perform time series-specific cross-validation or account for stationarity.
- **Scalability:** The code is intended for educational purposes and small datasets. For larger and more complex datasets, consider using specialized libraries and more robust pipelines.

## License

This project is licensed under the MIT License.  
See [LICENSE](LICENSE) for more details.

---

**Contributions, suggestions, and improvements are welcome!**

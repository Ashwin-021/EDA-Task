# Shopify Stock EDA

## 📊 Project Overview

This project performs Exploratory Data Analysis (EDA) on Shopify stock market data using Python.

The analysis explores historical stock prices, trading volume, moving averages, and daily returns to understand the behavior and trends in Shopify stock data.

## 🎯 Objectives

- Load and inspect Shopify stock data
- Understand the structure and statistics of the dataset
- Convert and sort the date column
- Analyze Open, High, Low, and Close prices
- Visualize Shopify stock price trends
- Analyze trading volume
- Calculate 20-day and 50-day moving averages
- Calculate daily returns
- Visualize the distribution of daily returns

## 📁 Dataset

The dataset contains Shopify historical stock market information.

### Columns

| Column | Description |
|---|---|
| `date` | Trading date |
| `open` | Opening stock price |
| `high` | Highest stock price during the trading day |
| `low` | Lowest stock price during the trading day |
| `close` | Closing stock price |
| `adj_close` | Adjusted closing price |
| `volume` | Number of shares traded |

The dataset contains **2,469 rows and 7 columns**, covering data from **May 21, 2015 to March 14, 2025**.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- Jupyter Notebook

## 🔍 Analysis Performed

### 1. Data Loading

The Shopify stock dataset is loaded using Pandas:

```python
df = pd.read_csv("/content/shopify_stock.csv")

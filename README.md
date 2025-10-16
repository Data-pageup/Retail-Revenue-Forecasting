# Retail Revenue Forecasting

## 📌 Project Overview
This project analyzes and forecasts monthly revenue for an e-commerce retail store using historical transaction data. The goal is to identify trends, seasonality, and future revenue patterns to support inventory planning, marketing, and business decisions.

---

## 🗂 Dataset
The dataset contains invoice-level transactions with the following columns:

| Column       | Description                             |
|-------------|-----------------------------------------|
| InvoiceNo   | Unique invoice identifier               |
| StockCode   | Product code                            |
| Description | Product description                     |
| Quantity    | Quantity purchased                       |
| InvoiceDate | Date and time of transaction             |
| UnitPrice   | Price per unit                            |
| Country     | Country of customer                       |

- **Data Cleaning**: Removed duplicates, negative values/returns, and missing data.  
- **Feature Engineering**: Added `TotalAmount = Quantity × UnitPrice` and aggregated revenue monthly.

---

## ⚙️ Methodology

### 1. Exploratory Data Analysis (EDA)
- Visualized monthly revenue trends.
- Identified top-selling products.
- Analyzed revenue distribution across countries.
- Detected seasonality (e.g., holiday spikes in Nov–Dec).

### 2. Forecasting Models
Implemented multiple models to predict monthly revenue:

| Model                                 | Description                                      | Parameters / Notes |
|--------------------------------------|-------------------------------------------------|------------------|
| **Linear Regression (LR)**           | Trend-based prediction using month index       | Simple linear regression |
| **ARIMA**                             | Non-seasonal time series                        | order=(2,1,2) |
| **SARIMA**                            | Seasonal time series with yearly seasonality   | order=(2,1,2), seasonal_order=(1,1,1,12) |
| **Simple Exponential Smoothing (SES)** | Level smoothing                                | α = 0.4 |
| **Double Exponential Smoothing (Holt)** | Level + Trend smoothing                         | α = 0.5, β = 0.3 |

### 3. Model Evaluation
- Forecasts were evaluated using **Mean Absolute Percentage Error (MAPE)**.  
- Visual comparison of **actual vs predicted** monthly revenue.

### 4. Future Forecast
- Predicted revenue for the next **6 months** using the best-performing models.  
- Forecast visualization done using **Plotly** for interactivity.

---

## 📊 Key Insights
- Revenue peaks during **November–December** (holiday season).  
- Certain products consistently generate the majority of revenue.  
- UK is the top-contributing country for sales.  
- Forecasts indicate stable growth in upcoming months post-holiday season.

---

## 🛠 Tools & Libraries
- **Python**: Core programming language  
- **Pandas & NumPy**: Data cleaning and aggregation  
- **Matplotlib & Seaborn**: Static visualizations  
- **Plotly Express**: Interactive charts  
- **Statsmodels**: ARIMA, SARIMA, SES, Holt forecasting  
- **Scikit-learn**: Linear Regression

---

## 🚀 Project Outcome
- Built a robust **forecasting pipeline** for monthly revenue.  
- Multiple models implemented to showcase **trend + seasonality handling**.  
- Clean, interactive visualizations suitable for **reporting or dashboards**.  
- Can be extended into a **Streamlit dashboard** for portfolio demonstration.

---

## 💼 Resume Line Example
> Forecasted e-commerce monthly revenue using Linear Regression, ARIMA, SARIMA, and Exponential Smoothing; identified trends and seasonality to optimize stock and marketing strategies.

---

- Showcase KPIs like last month revenue, growth %, top products, and forecast charts.  


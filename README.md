# 🌦️ Weather Forecasting and Seasonal Trend Analysis Using Time Series Models

This project focuses on analyzing historical weather data to uncover **trend, seasonality, cyclic variations, and forecasting future temperature values** using powerful **Time Series Analysis techniques**.  
The study applies classical statistical models such as **ARIMA, SARIMA**, and decomposition methods to extract meaningful insights from real-world weather data.


## 📌 **Project Overview**
The purpose of this project is to **forecast future temperatures** and extract meaningful weather-related patterns using historical data.  
The project covers:
- Trend analysis  
- Seasonal index calculation  
- Stationarity testing  
- Forecasting using ARIMA & SARIMA  
- Error evaluation  
- Visual insights  

This project helps understand **long-term weather patterns**, which can help in:
- Agriculture  
- Climate change analysis  
- Event planning  
- Environmental monitoring  

---

## 📊 **Dataset Description**
The dataset includes hourly/daily weather observations with the following key columns:

- `Formatted Date`
- `Temperature (C)`
- `Humidity`
- `Apparent Temperature`
- `Wind Speed`
- `Wind Bearing`
- `Visibility`
- `Pressure`
- `Daily Summary`

The data is converted to **time-indexed format** for time series modeling.

---

# 🧠 **Project Steps (1–7)**

## **1️⃣ Data Cleaning & Preprocessing**
- Converted `Formatted Date` to datetime  
- Set datetime as index  
- Checked and handled missing values  
- Resampled data (hourly → daily/monthly mean)  
- Removed outliers where necessary  
- Selected the target variable: **Temperature (C)**  

---

## **2️⃣ Exploratory Data Analysis (EDA)**
- Line plots to understand the trend  
- Histogram + KDE for distribution  
- Seasonal patterns (monthly averages)  
- Rolling mean & rolling standard deviation  
- Decomposition into:  
  - Trend  
  - Seasonal  
  - Residual components  

---

## **3️⃣ Stationarity Check**
To apply time series models, the series must be stationary.

Techniques used:
- **ADF (Augmented Dickey-Fuller Test)**
- Differencing (1st, 2nd)
- Visual check:  
  - Rolling mean  
  - Rolling std  

Stationarity confirmed before model training.

---

## **4️⃣ ACF & PACF Analysis**
Used to determine:
- AR (Auto Regression) order  
- MA (Moving Average) order  
- Seasonal periodicity  

Tools:
- ACF plot  
- PACF plot  

These help in selecting optimal ARIMA/SARIMA parameters.

---

## **5️⃣ ARIMA Model Training**
- Fit ARIMA model  
- Tuned parameters `(p, d, q)`  
- Generated in-sample predictions  
- Forecasted future temperature values  
- Compared with actual values  
- Plotted forecast vs real  

---

## **6️⃣ SARIMA Model Training**
Used when seasonal patterns found.

Model trained with:
- Non-seasonal part `(p, d, q)`
- Seasonal part `(P, D, Q, m)`

SARIMA captures both:
- Trend  
- Seasonality  

Forecast accuracy compared with ARIMA.

---

## **7️⃣ Model Comparison & Insights**
Evaluation metrics:
- RMSE  
- MAE  
- MAPE  

SARIMA showed better performance due to strong seasonality.

Forecast generated for:
- Next 7 days  
- Next 30 days  

---

# ⭐ **Features**
✔ Time series decomposition  
✔ Trend analysis (linear + rolling)  
✔ Seasonal index calculation  
✔ ACF & PACF plots  
✔ ARIMA & SARIMA forecasting  
✔ Test/train splitting  
✔ Error metrics (RMSE, MAE)  
✔ Visualization-rich project  
✔ Fully reproducible Python notebook  

---

## 🛠 **Tech Stack**
- **Python**
- pandas  
- numpy  
- matplotlib  
- seaborn  
- statsmodels  
- sklearn  
- pmdarima (auto_arima)  

---

# 🧹 **Data Preprocessing**
- Removed unnecessary columns  
- Converted timestamps  
- Handled missing values  
- Created daily average temperature series  
- Removed anomalies  
- Final dataset ready for time series modeling  

---

# 📈 **Time Series Analysis Techniques**
- Trend Analysis  
- Differencing  
- Seasonal Decomposition (Additive/Multiplicative)  
- ACF/PACF  
- Exponential Smoothing  
- ARIMA  
- SARIMA  

---

# 🤖 **Models Used**

### **🔹 ARIMA**
Good for non-seasonal data.  
Findings:
- Captured trend  
- Moderate accuracy  
- Not good with strong seasonality  

### **🔹 SARIMA**
Best performer.  
Findings:
- Captured both trend + seasonality  
- Most stable model  
- Lowest forecast error  

---

# 🔮 **Forecasting Results**
- Next 7 days forecast  
- Next 30 days forecast  
- Confidence intervals (95%)  
- Plots showing future trend  
- Seasonal effect clearly shown  

---

# 📌 **Key Insights**
- Temperature data has a **clear seasonal pattern**  
- Strong cyclic trends detected  
- SARIMA significantly outperforms ARIMA  
- Daily/Monthly seasonality affects temperature patterns  
- Useful for:  
  - Long-term weather planning  
  - Environmental monitoring  
  - Predictive analytics  

---

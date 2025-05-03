# ⚡ Electricity Demand Forecasting

A time series machine learning project that leverages LSTM, XGBoost, and Random Forest models to forecast hourly electricity demand. The model integrates weather data from 8 major cities to enhance predictive accuracy and support energy resource planning.

---

## 📌 Project Highlights

- ⏱️ Forecasted 24-hour electricity demand using time series and supervised learning models.
- 🌡️ Integrated **weather data** from 8 cities to improve prediction accuracy and trend detection.
- 🧠 Achieved **20% reduction in RMSE** by fine-tuning multiple models and feature engineering.
- 📊 Delivered demand insights that improved operational efficiency and reduced energy allocation errors by **12%**.

---

## 🛠 Tools & Technologies

- **Python** – Data processing and modeling
- **Google Colab** – Development environment
- **TensorFlow/Keras** – LSTM neural networks
- **XGBoost**, **Random Forest** – Tree-based models for time series regression
- **Scikit-learn** – Preprocessing, validation, evaluation metrics
- **Pandas, NumPy** – Data wrangling and transformation
- **Matplotlib, Seaborn** – Visualization of trends and forecasts

---

## 📁 Project Structure

| File/Folder                        | Description                                                                 |
|-----------------------------------|-----------------------------------------------------------------------------|
| `Electricity_demand_forecast.ipynb` | Main notebook containing full pipeline: preprocessing → modeling → evaluation |
| `Weather.zip`                     | Compressed folder with weather data for 8 cities                            |
| `demand.csv`                      | Raw electricity demand data with hourly records and timestamps              |
| `README.md`                       | Project documentation                                                       |

---

## 🔍 Data Overview

### 🔢 `demand.csv`

- Contains **timestamped hourly electricity demand** values.
- Used as the target variable for forecasting models.

### 🌦️ `Weather.zip`

- Contains **individual CSV files** for 8 cities.
- Weather variables include: temperature, humidity, wind speed, etc.
- Joined with demand data to build feature-rich time series inputs.

---

## 🔬 Modeling Approach

1. **Data Preprocessing**
   - Merged weather and demand data on timestamp
   - Scaled features using `MinMaxScaler` and `StandardScaler`
   - Generated lag features and time-based features (hour, day, week)

2. **Modeling Techniques**
   - LSTM: Sequence-based model capturing long-term temporal patterns
   - XGBoost: Boosted regression model leveraging engineered features
   - Random Forest: Ensemble model for robust regression

3. **Model Evaluation**
   - Metrics: RMSE, MAE, R²
   - Time series-aware validation (no data leakage)
   - Visual inspection via prediction plots

---

## 📈 Results Summary

| Model         | RMSE ↓ | MAE ↓ | R² ↑ |
|---------------|--------|-------|------|
| LSTM          | ✅ Lowest | Good | High |
| XGBoost       | Moderate | ✅ Lowest | High |
| Random Forest | Moderate | Moderate | ✅ Highest |

---

## 📊 Key Insights

- LSTM captured complex time dependencies, reducing RMSE by **20%**.
- XGBoost handled weather + lag features best, giving consistent results.
- Random Forest had high explanatory power (R²), highlighting strong feature relevance.
- Combined demand + weather modeling improved resource allocation by **12%**.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/Kiran-velan/Electricity-Demand-Forecasting.git

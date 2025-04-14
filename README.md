# 🌤️ Delhi Weather Forecasting & Anomaly Detection

This project performs data exploration, visualization, anomaly detection, time series decomposition, and forecasting of weather data (specifically Delhi's daily climate) using statistical methods and Facebook Prophet.

## 📌 Overview

The goal of this project is to understand and forecast the daily mean temperature in Delhi using a historical dataset. The script provides insights through:
- Exploratory Data Analysis (EDA)
- Correlation analysis
- Anomaly detection using Z-score
- Seasonal decomposition
- Forecasting with Prophet (with and without additional regressors)

---

## 🗃️ Dataset

**Source**: `DailyDelhiClimateTrain.csv`  
**Features**:
- `date`: Date of observation
- `meantemp`: Mean temperature (°C)
- `humidity`: Relative humidity (%)
- `wind_speed`: Wind speed (km/h)

---

## 🧰 Libraries Used

- `pandas`, `numpy` – Data manipulation
- `matplotlib`, `seaborn`, `plotly` – Data visualization
- `scipy.stats` – Z-score anomaly detection
- `statsmodels` – Seasonal decomposition
- `prophet` – Time series forecasting
- `sklearn.metrics` – Evaluation metrics

---

## 📊 Exploratory Data Analysis

Includes:
- Line plots showing trends over time for temperature, humidity, and wind speed
- Scatter plot showing the relationship between humidity and temperature
- Heatmap of correlations between features
- Monthly temperature trends year-over-year

---

## ⚠️ Anomaly Detection

Temperature anomalies are identified using the Z-score method:
- Any data point with a Z-score > 2 is considered an anomaly.
- These points are highlighted over the original temperature timeline.

---

## 🔍 Seasonal Decomposition

Using `seasonal_decompose`, the mean temperature is decomposed into:
- **Observed**
- **Trend**
- **Seasonality**
- **Residuals**

This helps understand the underlying patterns in the data.

---

## 🔮 Forecasting

### Prophet (Baseline)
- Forecasts future temperatures for 1 year (365 days).
- Evaluation using MAE and RMSE.

### Prophet with Regressors
- Incorporates `humidity` and `wind_speed` as additional predictors.
- Forecast is extended using last known regressor values.

---

## 📈 Evaluation Metrics

- **MAE** (Mean Absolute Error)
- **RMSE** (Root Mean Squared Error)

These help gauge the model's performance on historical data.

---

## 💻 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/weather-forecasting-delhi.git
   cd weather-forecasting-delhi
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the script:
   ```bash
   python weather_forecasting.py
   ```

---

## 📂 File Structure

```
├── weather_forecasting.py       # Main script
├── DailyDelhiClimateTrain.csv   # Dataset (make sure it's in the same directory)
├── README.md                    # Project documentation
└── requirements.txt             # Python dependencies
```

---

## 📌 Requirements

Create a `requirements.txt` like this:

```txt
pandas
numpy
matplotlib
seaborn
plotly
scipy
statsmodels
prophet
scikit-learn
```

---

## ✨ Visual Highlights

*(Add image links if available or generated)*

---

## 📬 Contact

For questions or suggestions:
- 📧 your.email@example.com
- 🐦 [@yourhandle](https://twitter.com/yourhandle)
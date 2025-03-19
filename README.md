# FBI Time Series Forecasting

## 📌 Project Overview
This project aims to forecast crime incident counts using time series analysis and machine learning models. The dataset consists of historical crime records, and the forecasting model helps predict future crime trends based on time-based patterns.

## 📂 Dataset
- **Train.xlsx**: Contains historical crime data, including date, time, type of crime, and location details.
- **Test.csv**: Used for evaluating the trained model.

## 🛠️ Tech Stack
- **Programming Language**: Python
- **Libraries**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Statsmodels, XGBoost, GeoPandas, Folium
- **Deployment**: Streamlit

## 📊 Exploratory Data Analysis (EDA)
Performed a thorough EDA to understand trends and seasonality:
- Yearly and monthly crime distributions.
- Crime trends by time of day (Morning, Afternoon, Evening, Night).
- Crime types and their occurrences.
- Geospatial analysis to visualize crime hotspots.
- Feature correlation analysis.

## 🔍 Time Series Analysis
- Seasonal decomposition to observe trends, seasonality, and residual components.
- Augmented Dickey-Fuller (ADF) and KPSS tests to check stationarity.
- First-order and seasonal differencing to make the data stationary.
- ACF and PACF plots for determining ARIMA/SARIMA parameters.

## 🚀 Model Training & Evaluation
### 1️⃣ **Statistical Models**
- **ARIMA**: Used for univariate time series forecasting.
- **SARIMA**: Captures seasonality in crime data.

### 2️⃣ **Machine Learning Models**
- **XGBoost Regressor**
- **Random Forest Regressor**

### ✅ Model Selection
Evaluation metrics used:
- **RMSE (Root Mean Squared Error)**
- **R² Score (Coefficient of Determination)**

🔹 **XGBoost** performed better with an **R² Score of 82.35%**, making it the final model for deployment.

## 🖥️ Deployment with Streamlit
A **Streamlit** app was built for predicting crime incident counts:
- Users upload a CSV with `YEAR`, `MONTH`, and `TYPE`.
- The app encodes categorical features, applies the trained model, and predicts incident counts.
- The results are downloadable as a CSV file.

## 📦 Model Storage & Deployment
- Trained **XGBoost** model saved as `xgboost_model.pkl` using `joblib`.
- Streamlit app script allows real-time predictions.

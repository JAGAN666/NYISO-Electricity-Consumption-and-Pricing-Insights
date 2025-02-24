# ⚡ NYISO Electricity Market Analysis & Forecasting  

## 📍 Project Overview  
This project explores **New York’s electricity market** using **NYISO pricing and load data**. The goal is to **predict electricity prices (LBMP), detect price anomalies, and forecast future electricity demand**. By leveraging **PySpark Structured Streaming, MLlib, and Sklearn**, this analysis provides insights into **grid operations, congestion effects, and demand patterns** that impact energy costs and availability.  

---

## 📊 Key Insights & Analysis  

### 🔥 1️⃣ Predicting Electricity Prices (LBMP) 💰  
- **Objective:** Predict **Locational Based Marginal Price (LBMP)** using **historical electricity demand** and grid conditions.  
- **Process:**  
  - Cleaned and preprocessed pricing & load datasets.  
  - Extracted **time-based features** (hour, day, month, season).  
  - Used **Linear Regression & Random Forest** models.  
  - Analyzed **correlation between load demand & LBMP**.  

- **Findings:**  
  - Electricity prices **spike during peak demand hours**.  
  - **Grid congestion** leads to localized LBMP fluctuations.  
  - **Weather & seasonal factors** impact energy prices.  

- **Model Performance:**  
  - **Linear Regression:** RMSE ~ **2.74**, R² ~ **0.85**  
  - **Random Forest:** RMSE ~ **2.19**, R² ~ **0.91**  

---

### ⚠️ 2️⃣ Detecting Price Anomalies  
- **Objective:** Identify **unexpected price surges** due to sudden changes in demand, congestion, or grid constraints.  
- **Process:**  
  - Used **Statistical Methods (Z-Score, IQR, Moving Average)** for anomaly detection.  
  - Applied **Time-Series Models** to detect deviations from historical trends.  
  - **Visualized** price fluctuations over time.  

- **Findings:**  
  - **Significant LBMP spikes** during grid congestion events.  
  - Higher **marginal costs for congestion/losses** increase electricity prices.  
  - **Anomalies often occur during extreme weather conditions.**  

---

### 🔮 3️⃣ Forecasting Future Electricity Demand  
- **Objective:** Forecast **Integrated Load (electricity demand)** using **historical LBMP and grid conditions**.  
- **Process:**  
  - Used **Structured Streaming** to process real-time energy data.  
  - Created **time-series features** (lags, rolling averages).  
  - Applied **ARIMA & LSTM (Neural Networks) models**.  

- **Findings:**  
  - **Winter and summer months** show **higher electricity demand** due to heating/cooling needs.  
  - **Peak energy consumption occurs in business districts & residential zones during evening hours**.  
  - **ARIMA performs well on short-term forecasts, while LSTM captures long-term patterns.**  

- **Model Performance:**  
  - **ARIMA:** RMSE ~ **1.98**, MAE ~ **1.45**  
  - **LSTM:** RMSE ~ **1.76**, MAE ~ **1.29**  

---

## 📂 Dataset & Features  
- **Pricing Data:** Locational Marginal Price (LBMP), congestion cost, loss cost.  
- **Load Data:** Integrated electricity demand, forecasted vs. actual consumption.  
- **Time Features:** Hourly, daily, seasonal trends affecting pricing & demand.  
- **Grid Conditions:** Transmission constraints, generation stability indicators.  

---

## 🛠️ Technical Implementation  

### 📥 Data Processing & Cleaning  
- Loaded **NYISO CSV files** into **PySpark** for **efficient big data handling**.  
- Handled missing values and **converted timestamps into structured features**.  
- Optimized performance using **PySpark SQL and VectorAssembler** for ML models.  

### 📊 Exploratory Data Analysis (EDA)  
- **Visualized demand trends** using **Matplotlib & Seaborn heatmaps**.  
- **Correlation analysis** revealed **strong links between LBMP & load demand**.  
- Created **interactive dashboards** to monitor price fluctuations.  

### 🤖 Machine Learning & Forecasting Models  
- **Linear Regression & Random Forest** → LBMP price prediction.  
- **Time-Series Models (ARIMA, LSTM)** → Electricity demand forecasting.  
- **Anomaly Detection (Z-Score, IQR, Moving Average)** → Identifying price spikes.  

### 📡 Structured Streaming for Real-Time Forecasting  
- Used **PySpark Streaming** to process **March, June, September, December** data in real-time.  
- Implemented **windowed aggregations** for forecasting LBMP & load trends.  
- **Deployed models for continuous price monitoring**.  

---

## 🚦 Key Business Applications  
✅ **Energy Market Optimization** → Helps utilities adjust pricing & demand response.  
✅ **Grid Stability & Planning** → Predicting congestion improves electricity distribution.  
✅ **Sustainability & Renewable Energy** → Optimizing integration of solar & wind power.  
✅ **Customer Cost Reduction** → Forecasting demand helps consumers manage energy use.  

---

## 📂 Repository Structure  

📂 NYISO-Electricity-Insights  
├── 📂 data/                # Raw & processed NYISO data  
├── 📂 notebooks/           # Google Colab notebooks  
├── 📂 models/              # Trained ML models for price forecasting  
├── 📂 visualizations/      # Charts, dashboards & analysis reports  
├── README.md              # Project summary & insights  
├── requirements.txt       # Dependencies (PySpark, Pandas, MLlib, Sklearn)  
└── LICENSE                # Open-source license  

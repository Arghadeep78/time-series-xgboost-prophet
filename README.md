# 🕒 Forecasting with XGBoost and Prophet  

A comprehensive time series forecasting project comparing **Facebook Prophet** (a decomposable additive model) and **XGBoost** (a gradient boosting algorithm).  
The project focuses on forecasting **hourly energy consumption** using the **PJME_hourly.csv** dataset, demonstrating an end-to-end approach — from exploratory data analysis (EDA) to model evaluation and comparison.

---

## 📘 Project Overview  

Accurate time series forecasting is vital for energy demand planning, anomaly detection, and load balancing.  
This project explores how **machine learning (XGBoost)** and **statistical modeling (Prophet)** perform on real-world hourly energy data.  

The workflow includes:  
1. **Data Preprocessing** — handling datetime features, missing values, and aggregations.  
2. **Feature Engineering** — extracting time-based features such as hour, day, and month.  
3. **Model Training** — fitting Prophet and XGBoost to the historical data.  
4. **Forecast Evaluation** — comparing models on MAPE, MAE, and MSE metrics.  
5. **Visualization** — plotting actual vs. predicted demand and trend components.

---

## 📂 Dataset  

**Source:** `PJME_hourly.csv`  
- Represents hourly energy consumption (megawatt usage) for the PJM East region.  
- Columns include:  
  - `Datetime`: Timestamp of the observation  
  - `PJME_MW`: Power consumption in megawatts  

> The dataset is publicly available from the [PJM Data Portal](https://datamarket.com/data/set/22r3/pjm-hourly-energy-consumption).

---

## ⚙️ Methods and Models  

| Model | Description | Type |
|-------|--------------|------|
| **Prophet** | Decomposable model capturing trend, seasonality, and holidays | Statistical |
| **XGBoost Regressor** | Tree-based ensemble boosting model using lag and date features | Machine Learning |

Both models are evaluated over the same test set for direct performance comparison.

---

## 📈 Evaluation Metrics  

The models are evaluated using the following metrics:

- **MAPE (Mean Absolute Percentage Error)**  
- **MAE (Mean Absolute Error)**  
- **MSE (Mean Squared Error)**  

These metrics measure forecast accuracy and penalize large deviations.

---

## 🧩 Key Results  

- Prophet effectively models **seasonality** and **long-term trends**.  
- XGBoost achieves **lower error metrics** after fine-tuning, performing better on **short-term fluctuations**.  
- Combining statistical decomposition with ML-based residual learning yields promising results.  

> Visualizations (such as actual vs. predicted plots) help illustrate where each model performs better.

---

## 🚀 How to Run  

```bash
# Clone the repository
git clone https://github.com/your-username/forecasting-with-xgboost-and-prophet.git
cd forecasting-with-xgboost-and-prophet

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook model.ipynb

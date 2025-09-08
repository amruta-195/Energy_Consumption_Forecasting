# Energy Consumption Forecasting ⚡

Predict electricity demand for a city or region using historical data.  
This project uses **ARIMA** (statistical model) and **LSTM** (deep learning model) to forecast energy consumption based on hourly energy usage data from the **PJM region** and individual companies like **AEP**.

---

## 📝 Project Overview

Energy demand forecasting is critical for:
- Smart-grid management
- Optimizing electricity production
- Reducing energy waste
- Supporting sustainable energy planning

This project demonstrates forecasting at both:
- **Individual company level** (e.g., AEP)
- **Regional level** (PJM Load)

---

## 📂 Dataset

- Source: [Kaggle PJM Hourly Energy Consumption Dataset](https://www.kaggle.com/datasets)
- Files used:  
  - `AEP_hourly.csv`  
  - `PJM_Load_hourly.csv`  
  - Additional company datasets: `COMED_hourly.csv`, `PJME_hourly.csv`, etc.  

**Columns:**  
- `Datetime` → Timestamp of measurement  
- `Value` → Energy consumption (MW)

---

## 🛠️ Technologies & Libraries

- Python 3.x
- Libraries:
  - `pandas`, `numpy` → Data handling
  - `matplotlib` → Visualization
  - `scikit-learn` → Metrics & preprocessing
  - `statsmodels` → ARIMA
  - `tensorflow/keras` → LSTM model

---

## 📈 Methodology

### 1. Data Preprocessing
- Convert `Datetime` to pandas datetime
- Set `Datetime` as index
- Resample hourly & fill missing values via interpolation
- Visualize historical consumption

### 2. Models Used
- **ARIMA**: Classical time-series forecasting model
- **LSTM**: Deep learning model for sequential data

### 3. Evaluation Metrics
- RMSE (Root Mean Squared Error)  
- MAE (Mean Absolute Error)

### 4. Forecasting
- Test set predictions
- 7-day future forecast

---

## 📊 Results

**Example Metrics (PJM Load):**

| Model | RMSE   | MAE    |
|-------|--------|--------|
| ARIMA | 6982.4 | 5305.8 |
| LSTM  | 630.3  | 471.1  |

**Observations:**  
- LSTM outperforms ARIMA in capturing non-linear patterns.  
- Future forecasts can help energy utilities plan ahead.

---

## 🖼️ Visualizations
- Historical consumption vs. predictions
- ARIMA vs LSTM comparison
- 7-day future forecast

*(Plots are generated in the notebook.)*

---

## 💻 How to Run

1. Clone the repository:
```bash
git clone https://github.com/amruta-195/Energy_Consumption_Forecasting.git
```
2.Install required libraries:
```bash
pip install -r requirements.txt
```

3.Open Jupyter Notebook:
```
jupyter notebook Energy_Forecasting.ipynb

```
4.Run all cells to reproduce results and plots.

## 🔗 References

- [PJM Hourly Energy Consumption Dataset (Kaggle)](https://www.kaggle.com/datasets)
- [ARIMA: statsmodels documentation](https://www.statsmodels.org/stable/index.html)
- [LSTM: Keras LSTM tutorial](https://keras.io/guides/sequential_model/)

---

## 📄 License

This project is for **educational purposes** and **internship use**.


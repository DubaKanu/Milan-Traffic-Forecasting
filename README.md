# Milan Traffic Forecasting

## Comparative Time Series Analysis and Forecasting of Mobile Network Traffic

**Author:** Josephine Duba Kanu
**Institution:** African Leadership University
**Course:** Machine Learning Techniques - I
**Date:** May 2026

---

## Project Overview

This project analyzes and forecasts real-world mobile internet traffic data 
from the city of Milan, Italy, released by Telecom Italia Mobile (TIM) as 
part of their Big Data Challenge. The dataset covers 10,000 geographical 
areas over two months, with traffic recorded every 10 minutes.

---

## Models Implemented

| Model | Type | MAE (Area 5181) |
|-------|------|----------------|
| Holt-Winters | Classical Statistical | 16.19 |
| LSTM | Neural Network | 6.49 |
| GRU | Neural Network | 7.05 |

**Best Model: LSTM** — achieved lowest MAE and RMSE across majority of areas.

---

## Repository Structure
Milan-Traffic-Forecasting/
├── Milan_Traffic_Forecasting.ipynb  ← Main notebook (all code)
├── README.md                         ← This file
├── requirements.txt                  ← Required libraries
├── area_5181.csv                     ← Highest traffic area data
├── area_4159.csv                     ← Area 4159 time series data
├── area_4556.csv                     ← Area 4556 time series data
├── task2_pdf.png                     ← PDF plot of traffic distribution
├── task2_timeseries.png              ← Time series plots
├── task2_stationarity.png            ← Stationarity analysis plot
├── task2_decomposition.png           ← Decomposition plot
├── task2_acf_pacf.png                ← ACF and PACF plots
├── task2_heatmap.png                 ← Spatial heatmap of Milan
├── task3_hw_predictions.png          ← Holt-Winters predictions
├── task3_lstm_predictions.png        ← LSTM predictions
└── task3_gru_predictions.png         ← GRU predictions

---

## How to Run the Code

### Requirements

First install all required libraries:

pip install -r requirements.txt
Or install manually:

pip install pandas numpy matplotlib scikit-learn statsmodels tensorflow jupyter

---

### Option 1: Google Colab (Recommended)

1. Go to [Google Colab](https://colab.research.google.com)
2. Click **File → Upload notebook**
3. Upload `Milan_Traffic_Forecasting.ipynb`
4. Click **Runtime → Run all**
5. When prompted, mount your Google Drive
6. Upload the CSV data files to your Google Drive under a folder called `milan_traffic`

---

### Option 2: Local Machine — Windows

1. Install Python 3.8+ from https://www.python.org
2. Open Command Prompt and run:

git clone https://github.com/DubaKanu/Milan-Traffic-Forecasting.git
cd Milan-Traffic-Forecasting
pip install -r requirements.txt
jupyter notebook Milan_Traffic_Forecasting.ipynb

---

### Option 3: Local Machine — macOS

1. Open Terminal and run:
git clone https://github.com/DubaKanu/Milan-Traffic-Forecasting.git
cd Milan-Traffic-Forecasting
pip install -r requirements.txt
jupyter notebook Milan_Traffic_Forecasting.ipynb

---

### Option 4: Local Machine — Linux

1. Open Terminal and run:
git clone https://github.com/DubaKanu/Milan-Traffic-Forecasting.git
cd Milan-Traffic-Forecasting
pip install -r requirements.txt
jupyter notebook Milan_Traffic_Forecasting.ipynb

---

## Dataset

The minimum data needed to run the forecasting models is included in this repository:
- `area_5181.csv` — Time series for the highest traffic area
- `area_4159.csv` — Time series for Area 4159
- `area_4556.csv` — Time series for Area 4556

The full 5GB dataset can be downloaded from:
- **Kaggle:** https://www.kaggle.com/datasets/freckled/telecom
- **Harvard Dataverse:** https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EGZHFV

---

## Key Results

### Performance Metrics

**Area 5181 (Highest Traffic Area)**

| Model | MAE | RMSE | MAPE (%) |
|-------|-----|------|----------|
| Holt-Winters | 16.19 | 17.84 | 129.66 |
| LSTM | 6.49 | 9.07 | 42.02 |
| GRU | 7.05 | 9.31 | 48.83 |

**Area 4159**

| Model | MAE | RMSE | MAPE (%) |
|-------|-----|------|----------|
| Holt-Winters | 42.07 | 59.38 | 46.45 |
| LSTM | 36.58 | 50.32 | 44.01 |
| GRU | 36.06 | 50.26 | 42.40 |

**Area 4556**

| Model | MAE | RMSE | MAPE (%) |
|-------|-----|------|----------|
| Holt-Winters | 91.94 | 122.24 | 45.48 |
| LSTM | 82.13 | 111.02 | 42.36 |
| GRU | 86.34 | 112.65 | 46.08 |

---

## Training Time

| Model | Avg Train Time | Avg Pred Time |
|-------|---------------|---------------|
| Holt-Winters | 1.52 seconds | 0.05 seconds |
| LSTM | 182.18 seconds | 122.88 seconds |
| GRU | 209.67 seconds | 125.72 seconds |

---

## References

1. Barlacchi et al., "A multi-source dataset of urban life in Milan," Scientific Data, 2015.
   https://doi.org/10.1038/sdata.2015.55

2. Hochreiter & Schmidhuber, "Long short-term memory," Neural Computation, 1997.
   https://doi.org/10.1162/neco.1997.9.8.1735

3. Cho et al., "Learning phrase representations using RNN encoder-decoder," EMNLP, 2014.
   https://doi.org/10.3115/v1/D14-1179

4. Chung et al., "Empirical evaluation of gated recurrent neural networks," arXiv, 2014.
   https://arxiv.org/abs/1412.3555

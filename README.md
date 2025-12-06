# Dual Prediction of Blood Pressure and Blood Glucose Level using PPG Signals  
## Exploring Deep Learning Models through Comparative Study

This repository contains the implementation and experimental workflow for the research paper **“Dual Prediction of Blood Pressure and Blood Glucose Level using PPG Signals: Exploring Deep Learning Models through Comparative Study.”**

The work proposes a **non-invasive framework** for simultaneously predicting **blood pressure (BP)** and **blood glucose (BG)** levels using **photoplethysmogram (PPG) signals**, leveraging deep learning and machine learning models.

---

## 📌 Abstract

Continuous monitoring of blood pressure and blood glucose is critical for managing chronic conditions such as hypertension and diabetes. However, conventional measurement techniques are invasive, uncomfortable, and unsuitable for long-term monitoring.

This project presents a **hybrid LSTM–XGBoost model** for **dual prediction of BP and BG** using PPG signals.  
- **LSTM** is used to capture temporal patterns present in PPG signals  
- **XGBoost** enhances prediction accuracy through feature selection and regression  

The proposed non-invasive framework demonstrates promising performance, achieving:
- **RMSE of 8.014 mg/dL** for blood glucose prediction  
- **MAE of 25.336 mmHg** for blood pressure estimation  

These results show the potential of wearable, cuff-less, and pain-free monitoring systems for real-world healthcare applications.

---

## 🧠 Methodology Overview

The system follows a two-stage modeling approach:

1. **PPG Signal Preprocessing**
   - Band-pass filtering (0.5–8 Hz)
   - Downsampling
   - Data augmentation using Gaussian noise
   - Normalization and dataset splitting

2. **Hybrid Model Architecture**
   - LSTM network for temporal feature extraction
   - Feature fusion with raw PPG signals
   - XGBoost regressor for final BP and BG prediction
   - K-Fold Cross-Validation for robustness

Separate models are trained for:
- Blood Glucose Prediction
- Blood Pressure Prediction

---

## 📊 Datasets Used

### 1. Blood Glucose Dataset
- 67 PPG samples collected from 23 subjects  
- Fingertip PPG captured using a green LED sensor  
- Reference glucose measured using Accu-Chek™ Active device  
- Dataset includes raw signals, labels, and signal visualizations  

### 2. Blood Pressure Dataset
- Publicly available PhysioNet dataset  
- Includes PPG, ECG, and ABP signals  
- Sampling frequency: 125 Hz  
- Used for cuff-less BP estimation  

> ⚠️ Due to privacy and licensing constraints, datasets are **not included** in this repository. Links and references are provided in the paper.

---

## 📈 Results Summary

### Blood Glucose Prediction
| Model | RMSE |
|------|------|
| CNN + GRU | 26.2 |
| CNN + GRU + FC + Regression | 19.66 |
| CNN + GRU + K-Fold | 17.8 |
| **LSTM + XGBoost (Proposed)** | **8.014** |

### Blood Pressure Prediction
| Model | RMSE |
|------|------|
| Linear Regression | 27.3 |
| Deep Learning (Dense Layers) | 25.9 |
| DL + BatchNorm + Bagging | 25.37 |
| **LSTM + XGBoost (Proposed)** | **25.336** |

---
If you use this work, please cite:
Priyavarshini G R, Indra Bhooshan Sharma,
"Dual Prediction of Blood Pressure and Blood Glucose Level using PPG Signals:
Exploring Deep Learning Models through Comparative Study",
International Research Journal on Advanced Science Hub, Vol. 07, Issue 12, 2025.

└── README.md


# Laoag River Water Level Forecasting (LSTM) — Training Code (ver1.0)

This repository contains the **training / evaluation / inference code** for the Laoag River AI-based flood forecasting project (LSTM-based water level prediction).

> **Version policy (ver1.0)**  
> This version corresponds to the **current Rating Curve (RC) setting** used in the project.  
> If the Rating Curve is updated/improved in the future, the model must be **re-trained** using the updated RC-derived water level data.  
> In that case, a new version (e.g., ver1.1, ver2.0) should be created and archived separately.

---

## 1. Project Overview

- **Goal:** Predict river water levels at multiple stations using LSTM-based soft-sensing.
- **Time interval:** 10-minute resolution time series.
- **Inputs (features):**
  - Rainfall gauges: `RG01` ~ `RG11`
  - Water levels (current): `WLxx` (station-wise, depending on dataset setup)
- **Outputs (targets):**
  - Future water level(s) at target station(s) after a given lead time.
- **Lead time examples (10-min step-based):**
  - 1 hour = `k = 6`
  - 3 hours = `k = 18`
  - 6 hours = `k = 36`

---

## 2. Environment & Dependencies

This codebase was developed and tested under the following environment:

- **Python:** 3.11.5  
- **OS:** Windows 10 (AMD64)  
- **conda:** True  
- **Keras backend:** TensorFlow  
- **GPU:** None (CPU-only)  
- **CUDA/cuDNN:** None / None  

### Package versions
- numpy==1.24.3  
- pandas==2.0.3  
- scikit-learn==1.3.0  
- joblib==1.2.0  
- h5py==3.9.0  
- tensorflow==2.15.0  
- keras==2.15.0  
- keras-tuner==1.4.7  
- matplotlib==3.8.3  

---

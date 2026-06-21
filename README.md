# ⚡ Voltage Stability Monitoring using PMU Data
**IEEE 39-Bus System · 50Hz Indian Grid Standard · VJTI Mumbai**

## Problem
Power grid voltage instability causes blackouts. India's 2012 
blackout affected 700 million people. This project builds an 
AI-based early warning system using PMU data to predict 
voltage collapse before it happens.

## Results
| Model | Approach | Danger Recall | F1 Score |
|---|---|---|---|
| Random Forest | Snapshot classification | 41% | 0.44 |
| XGBoost | Snapshot classification | 42% | 0.46 |
| LSTM Binary | Trajectory prediction | **84%** | **0.58** |

## Dataset
- 18,213 synthetic PMU readings
- IEEE 39-bus system (50Hz Indian grid standard)
- 468 simulations: 13 load factors × 35 N-1 contingencies
- Labels: STABLE / WARNING / UNSTABLE

## Notebooks
| Notebook | Description |
|---|---|
| 01_system_setup_simulation | IEEE 39-bus setup, power flow, PV curve |
| 02_dataset_generation | PMU dataset via N-1 contingency simulation |
| 03_eda_feature_engineering | EDA, correlation, stress index feature |
| 04_ml_models | Random Forest + XGBoost with class weighting |
| 05_lstm_early_warning | LSTM binary early warning system |

## Tech Stack
Python · pandapower · scikit-learn · XGBoost · 
TensorFlow/Keras · pandas · NumPy · matplotlib

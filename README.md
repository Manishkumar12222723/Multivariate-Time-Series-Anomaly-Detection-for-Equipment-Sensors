Multivariate Time-Series Anomaly Detection for Equipment Sensors

📌 Project Overview

This project focuses on detecting anomalies in multivariate time-series sensor data collected from industrial equipment. The objective is to identify abnormal patterns that may indicate equipment failure, degradation, or operational instability.

The workflow includes:

Data preprocessing

Feature extraction (time-based + statistical)

Modeling using:
✔ Isolation Forest
✔ LSTM Autoencoder

Evaluation & visualization of detected anomalies

📂 Dataset Description

File: equipment_sensors.csv

Column	Description
timestamp	Time index (min-level resolution)
temp	Temperature sensor
vibration	Vibration level sensor
rpm	Rotational speed
pressure	Pressure output

Data characteristics:

Temporal dependency

Correlated sensor variables

Continuous real-valued measurements

🏗 Technologies Used
Programming

Python 3.x

Libraries

pandas

numpy

scikit-learn

tsfresh

tensorflow / keras

matplotlib / seaborn

jupyter

🚀 Project Pipeline
1. Data Loading & Cleaning

parse timestamps

set time index

handle missing values

smoothing (optional)

2. Feature Engineering

Feature categories used:

✔ Statistical (mean, std, kurtosis, skewness)
✔ Rolling window features
✔ FFT/energy features
✔ Autocorrelation
✔ Time deltas

tsfresh automates extraction and relevance filtering.

3. Model 1: Isolation Forest

Algorithm detects outliers in feature space by:

random partitioning

anomaly scoring via path length

Advantages: Fast, unsupervised, multivariate capable

4. Model 2: LSTM Autoencoder

Sequence learning approach:

Encoder compresses temporal window

Decoder reconstructs signal

Reconstruction error ↗ = anomaly

Suitable for temporal patterns & correlations.

5. Evaluation Metrics

Used:

Precision

Recall

F1-score

AUC (optional for scoring)

Reconstruction error visualization

Anomaly timelines

6. Visualization Outputs

Charts included in the notebook:

📈 Multivariate sensor plot
📉 Reconstruction error plot
🔍 Anomaly heatmap / scatter
⏱ Timeline anomaly tagging

📁 Deliverables

☑ notebook.ipynb — complete implementation
☑ equipment_sensors.csv — dataset
☑ figures/ — plots & visualizations
☑ README.md — documentation
☐ (optional) model.h5 — saved LSTM weights

⚙ Run Instructions
1. Install Dependencies
pip install pandas scikit-learn tsfresh tensorflow keras matplotlib seaborn

2. Run Notebook
jupyter notebook


Open notebook.ipynb and execute step-by-step.

🎯 Use Cases

This solution applies to:

Predictive maintenance

Condition monitoring

IoT device monitoring

Industrial automation

Manufacturing & plant operations

📌 Future Enhancements

Possible extensions:

✔ Online/streaming inference
✔ GRU/Transformer models
✔ Root cause analysis
✔ Sensor fusion
✔ Edge deployment

# Machine Learning Based Traffic Flow Prediction Using V2X Communication Data

This repository documents our research work on traffic flow prediction using Vehicle-to-Everything (V2X) communication data.

## Paper Details

- **Title:** Machine Learning Based Traffic Flow Prediction Using V2X Communication Data
- **Authors:** Varun Kumar, Rahul Paul, Vaidya Parth Kishor, Yuvank Goyal, Avdhesh Mandloi
- **Institution:** IIIT Vadodara - International Campus Diu
- **Status:** Accepted at RECCAP 2026, IIT Palakkad

## Problem Statement

Modern cities require real-time and computationally efficient systems for traffic monitoring and congestion prediction. This work focuses on traffic congestion prediction using V2X communication data.

## Dataset

- **Source:** Simulated V2X records generated using SUMO and VEINS
- **Size:** 10,000 records
- **Features:** vehicle speed, vehicle density, GPS latitude, GPS longitude, time of day, acceleration
- **Target:** traffic flow level in vehicles per hour

## Data Preprocessing

The preprocessing pipeline includes:

- Missing value handling
- Median imputation
- Min-Max normalization
- IQR-based outlier removal
- 80/20 train-test split

## Model

- **Primary model:** Linear Regression

## Evaluation Metrics

| Metric | Value |
| --- | --- |
| R² Score | 0.87 |
| MAE | 3.21 veh/hr |
| RMSE | 4.56 veh/hr |
| Training Time | 0.43 s |
| Inference Time | < 1 ms |

## System Pipeline

1. V2X data acquisition
2. Data preprocessing
3. ML inference
4. Congestion class prediction
5. GUI map visualization

## GUI Features

- Color-coded congestion map
- Manual feature input
- Prediction output
- Rolling history chart
- Heavy congestion alerts

## Comparative Analysis

| Model | R² Score | MAE | Notes |
| --- | ---: | ---: | --- |
| Linear Regression | 0.87 | 3.21 | Lightweight and interpretable |
| Random Forest | 0.91 | 2.85 | Higher accuracy but higher inference time |
| SVR | 0.83 | 3.65 | Lower predictive performance |

## Key Conclusion

Linear Regression provides a lightweight and interpretable model suitable for real-time traffic flow prediction.

## Limitations

- Simulation-based dataset
- No live C-V2X/5G hardware testing
- Limited handling of accidents, weather effects, and non-linear behavior

## Future Work

- Live V2X integration
- LSTM and Gradient Boosted Trees
- More V2X event types
- Federated learning
- Smart city pilot testing

## Repository Status

This repository currently serves as a public project page and documentation space for the accepted research paper. Production code and datasets are not claimed to be available at this stage and may be added later.

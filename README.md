AI in Enhancing CyberScurity Incident Response
# AI-based Anomaly Detection for Network Traffic

This project implements a Recurrent Neural Network (RNN) using an LSTM (Long Short-Term Memory) model to detect anomalies in network traffic data. The anomalies represent potential security incidents, and the system triggers an incident response workflow with severity levels and actions taken based on the detected anomaly scores.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Technologies Used](#technologies-used)
4. [Setup](#setup)
5. [Usage](#usage)
6. [Incident Response Workflow](#incident-response-workflow)
7. [Visualization](#visualization)
8. [Future Enhancements](#future-enhancements)

## Project Overview
The project aims to detect anomalies in network traffic, which can signify possible security threats. We use an LSTM model to predict traffic patterns based on past data. Any significant deviation from the expected traffic is flagged as an anomaly. This is followed by an incident response mechanism that categorizes the severity of the incident and initiates appropriate actions.

## Features
- **Data Preprocessing**: Time-series data preparation, including feature scaling and creating supervised sequences for the LSTM model.
- **LSTM-based Prediction**: Recurrent Neural Network (LSTM) for predicting normal network traffic behavior.
- **Anomaly Detection**: Automatically identifies anomalies using a threshold-based method.
- **Incident Response**: Triggers an incident response workflow based on the anomaly's severity (Critical, High, Low).
- **Visualization**: Graphs to visualize predicted traffic, actual traffic, and anomalies.
- **Severity Classification**: Incidents are classified into different severities based on the anomaly score.

## Technologies Used
- **Python 3.x**
- **Keras** (with TensorFlow backend)
- **NumPy** & **Pandas** (for data handling)
- **Matplotlib** & **Seaborn** (for data visualization)
- **scikit-learn** (for preprocessing)

## Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/anomaly-detection-lstm.git
    cd anomaly-detection-lstm
    ```

2. Install the dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the script:
    ```bash
    python anomaly_detection.py
    ```

## Usage
1. Modify the dataset or use the simulated data included in the project. You can replace the traffic data with real-world network traffic data in `pandas DataFrame` format.
2. Adjust the `sequence_length` and other hyperparameters in the script as needed.
3. The LSTM model will predict traffic, and deviations from expected values will be flagged as anomalies.
4. Review the log of incidents and visualize the anomalies detected.

## Incident Response Workflow
When an anomaly is detected, the system triggers an incident response workflow based on the anomaly score:

- **Critical**: Immediate action is taken (e.g., shutdown or investigation).
- **High**: Alerts are sent to the Security Operations Center (SOC) team.
- **Low**: Logged for review, but no immediate action required.

## Visualization
The project includes graphs for:

-**Training Loss**: Visualizes how the LSTM model's loss decreases over training epochs.
-**Anomaly Detection**: Displays actual and predicted network traffic with anomalies highlighted.
-**Severity Count**: A bar chart showing the distribution of detected incidents by severity.

## Future Enhancements
- Integrate real-world network traffic datasets for a more robust system.
- Implement a more advanced anomaly detection method (e.g., using autoencoders or GANs).
- Add real-time anomaly detection and alerting.


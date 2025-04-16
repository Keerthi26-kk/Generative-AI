
Real-Time Fraud Detection System Using Streaming Data

• Overview

This project simulates a real-time fraud detection system for financial transactions using machine learning. It demonstrates how a cloud-ready solution can detect fraudulent transactions on the fly, with features such as live prediction, anomaly detection, and statistical monitoring — all within a Jupyter Notebook environment.

The system uses an Isolation Forest algorithm trained on transactional features and streams new transactions one by one, mimicking a real-world data pipeline.

Cloud-aligned project without incurring cloud storage costs — built for Data Science + MLOps readiness.

• Dataset Features

The model is trained on transaction data containing the following key fields:

amount – Transaction amount
oldbalanceOrg – Sender's original balance
newbalanceOrig – Sender's balance after transaction
oldbalanceDest – Recipient's original balance
newbalanceDest – Recipient's balance after transaction

• Project Workflow

Data Loading & Cleaning
Reads a .csv file of transaction records.
Cleans missing values and selects relevant features.
Model Training
Trains an IsolationForest model to detect anomalies based on transaction behavior.
Saves the trained model using joblib.
Real-Time Streaming Simulation
Simulates a stream of transactions one-by-one using a for loop and time.sleep().
Makes predictions in real time and logs the fraud alerts.
Logging & Monitoring
Logs detected frauds into a fraud_log.csv.
Displays running fraud statistics and summary.

• Key Features

Real-time fraud detection (stream simulation)
Model-based anomaly prediction (unsupervised)
Live statistical tracking (fraud rate, counts)
Fraud logging with CSV output
Cloud-aligned design (no actual deployment required)

• Tech Stack


Tool / Library	Purpose
Python (Pandas, Sklearn)	Data processing and modeling
Isolation Forest	Anomaly detection algorithm
Joblib	Model serialization
CSV Writer	Fraud transaction logging
Matplotlib (optional)	Real-time visualization (optional)
Jupyter Notebook	Development & simulation environment

• Future Enhancements

Add SHAP-based model explainability
Integrate with message alerts (Slack, email)
Implement real-time dashboards (e.g., Streamlit)
Add auto-retraining based on fraud pattern drift
Use Kafka or AWS Kinesis for true real-time ingestion

• Business Impact

Detect fraudulent activity in near real-time
Reduce false positives with anomaly detection
Improve fraud handling efficiency
Build MLOps-ready systems with minimal infrastructure

• Cloud-Ready Design

While the solution runs locally in a notebook, its modular architecture is designed for easy integration with:

AWS S3 (for dataset storage)
SageMaker (for model training/deployment)
CloudWatch/SNS (for alerting)
Lambda (for serverless processing)

# AI-Driven Cybersecurity Threat Detection System
## Overview
This project collects internal and external security events, runs ML inference to score/prioritize threats, records events and remediation actions into local and centralized MySQL, provides a JavaFX GUI with hourly charts, and sends notifications via email/SMS.It helps in identifying suspicious activities, anomalies, or malicious patterns in data.

---

## 🎯 Problem Statement

Traditional cybersecurity systems rely on rule-based detection, which fails to identify new and evolving threats.

This project aims to:

* Detect anomalies in system/network behavior
* Identify potential cyber threats
* Improve security using AI-based models

---

##  Features

* 🧠 AI-based threat detection
* 📊 Data analysis for anomaly detection
* ⚡ Automated detection system
* 📈 Visualization of suspicious patterns
* 🔍 Identifies unusual activities

---

##  Tech Stack

* Python
* Machine Learning
* Pandas, NumPy, Scikit-learn

---

##  Project Workflow

1. Data Collection (network/security dataset)
2. Data Cleaning & Preprocessing
3. Model Training (ML algorithm)
4. Threat Detection
5. Result Visualization

---

## 📸 Output Screenshots
<img width="1455" height="848" alt="output" src="https://github.com/user-attachments/assets/76b31ee4-0a6d-4e21-affa-59c8e6b29311" />

---
## Components
- python/ : ingestion, feature extraction, model training & Flask inference service
- java/ : JavaFX GUI, DB manager, notification clients, inference client
- mysql/ : schema + sample data
- docs/ : architecture, deployment

## Quickstart (Local)
1. Setup MySQL:
   - `mysql -u root -p < mysql/schema.sql`
2. Python:
   - `cd python`
   - `pip install -r requirements.txt`
   - Train (if you have training data): `python models/train.py`
   - Run API: `python api/app.py` (listens on port 5000)
3. Java:
   - Edit `src/main/resources/application.properties` with DB & notifier creds and inference endpoint `http://localhost:5000`
   - `mvn clean package`
   - Run `java -jar target/cybersec-solution-1.0.0.jar`
4. Configure connectors to forward logs to `python/ingest` or call Java `InferenceClient` with raw events.

## Alerts
- Configure email credentials (SMTP) and Twilio in `application.properties` for production alerts.

## Security & Hardening Notes
- Use TLS for inference and DB connections.
- Use least-privilege DB users.
- Rotate API keys and secrets (do NOT store in repo; use env or vault).
- Use rate limiting and authentication on the Flask API (JWT or mTLS).

## 📈 Results

* Achieved **X% accuracy** in detecting anomalies
* Successfully identified suspicious patterns
* Reduced manual monitoring effort

---

## 🔮 Future Improvements

* Real-time intrusion detection system
* Integration with firewalls
* Deep learning-based threat detection
* Deployment as a web dashboard

---

## 💡 Applications

* Network Security Monitoring
* Fraud Detection
* Intrusion Detection Systems
* Enterprise Security

# Predictive Maintenance System using Edge ML

## Overview  
This project implements an IoT and machine learning-based predictive maintenance system. It captures temperature and vibration data from sensors, runs inference at the edge on ESP32, and relays prediction results and alerts to a web dashboard for visualization and monitoring.

## Implementation Approach  
- Sensor data i.e temperature, vibration is collected by an ESP32 microcontroller.  
- Edge computing: a trained Random Forest model runs locally on the ESP32 to detect anomalies or potential failures.  
- When predictions are made, relevant data and alerts are forwarded to a backend server.  
- A simple web dashboard displays real-time equipment status, predictions, and alerts to users.  
- Initial model training and validation use a Kaggle dataset; live sensor data feeds into prediction pipeline thereafter.

## Key Components & Technologies  
- **Microcontroller / Edge device**: ESP32 (programmed via Arduino IDE)  
- **Sensors**: temperature Sensor, vibration sensor  
- **ML Model**: Random Forest (classification)  
- **Backend**: Web server (telegraf)to receive data, store logs, and relay to UI  
- **Dashboard**: Web-based front end for visualization and alert management via Chronograf

## Feature Pipeline  
- Preprocessing: filtering, handling missing values, feature extraction 
- Feature selection: select relevant predictors  
- Model training: train Random Forest on historical data, validate with metrics  
- Deployment: deploy compact model on ESP32 for continuous inference  

## Usage & Interaction  
- Users, admins access the dashboard via browser to view system health and alerts  
- The ESP32 autonomously monitors in real time and triggers alerts when anomalies exceed thresholds  

## Status & Roadmap  
- [ ] Data collection and model training with public dataset  
- [ ] Edge deployment and inference testing  
- [ ] Dashboard development and alerting interface  
- [ ] Real-world validation and tuning  
- [ ] Performance optimization and scaling

## Acknowledgments  
- Public datasets from Kaggle  
- Open-source libraries and frameworks used  


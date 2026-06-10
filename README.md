# Federated Learning-Based Intrusion Detection System (FL-IDS)

A Privacy-Preserving and Zero-Day Attack Detection Framework for Cybersecurity using Federated Learning, Differential Privacy, Deep Learning, and Machine Learning.

---

## Overview

Cyberattacks are becoming increasingly sophisticated, making traditional Intrusion Detection Systems (IDS) less effective against modern threats and previously unseen attacks. At the same time, organizations face strict privacy requirements that prevent centralized sharing of security data.

This project presents a **Federated Learning-Based Intrusion Detection System (FL-IDS)** that addresses both challenges by combining:

- Federated Learning
- Differential Privacy
- Deep Learning-based Intrusion Detection
- Autoencoder-based Zero-Day Attack Detection
- Machine Learning Classification
- Fusion-Based Threat Analysis

The system enables multiple clients to collaboratively train intrusion detection models without sharing raw data while maintaining privacy and improving attack detection capabilities.

---

# Project Objectives

- Detect malicious network traffic and cyberattacks.
- Preserve user and organizational privacy during training.
- Simulate distributed federated learning environments.
- Detect previously unseen (Zero-Day) attacks.
- Reduce false positives using fusion-based decision making.
- Improve cybersecurity resilience through collaborative learning.

---

# Key Features

## Federated Learning

- Distributed client training
- Local model updates
- Global model aggregation
- No raw data sharing between clients

## Differential Privacy

- Privacy-preserving training
- Gradient clipping
- Noise injection
- Protection against information leakage

## Zero-Day Attack Detection

- Autoencoder-based anomaly detection
- Reconstruction error analysis
- Detection of unseen attacks

---

# Datasets Used

## UNSW-NB15 Dataset

The UNSW-NB15 dataset is used for intrusion detection and attack classification.

Attack categories include:

- Analysis
- Backdoor
- DoS
- Exploits
- Fuzzers
- Generic
- Reconnaissance
- Shellcode
- Worms

The dataset is processed into binary labels:

- Normal Traffic
- Malicious Traffic

---

## IoT-23 Dataset

The IoT-23 dataset is used for malware and malicious IoT traffic analysis.

The dataset contains:

- Benign Traffic
- Malware Traffic
- Suspicious Traffic

---

# System Architecture

```text
                        +-------------------+
                        |   Global Dataset  |
                        +---------+---------+
                                  |
                                  v

                    +--------------------------+
                    | Data Preprocessing Layer |
                    +------------+-------------+
                                 |
             -----------------------------------------
             |                |               |      |
             v                v               v      v

        Client 1         Client 2        Client 3  Client 4

             |                |               |      |
             |                |               |      |
             +----------------+---------------+------+
                                 |
                                 v

                     Federated Learning Layer

                                 |
                                 v

                     Differential Privacy Layer

                                 |
                                 v

                      Global Model Aggregation

                                 |
                                 v

               ----------------------------------
               |                                |
               v                                v

      Intrusion Detection Module      Zero-Day Detection Module

               |                                |
               +---------------+----------------+
                               |
                               v

                    Fusion-Based Decision Engine

                               |
                               v

                      Final Threat Classification
```

---

# Module 1: Differential Privacy Based Federated IDS

## Objective

Enable collaborative intrusion detection while preserving data privacy.

In traditional centralized learning, all client data is collected in a single location, creating privacy and security risks.

Federated Learning solves this by allowing clients to train models locally and only share model updates.

---

## Differential Privacy

To further protect sensitive information, Differential Privacy is integrated into the federated learning process.

The privacy mechanism introduces carefully calibrated noise into model updates before aggregation.

Benefits include:

- Protection against model inversion attacks
- Protection against data reconstruction attacks
- Enhanced user privacy
- Secure collaborative learning

---

## Workflow

```text
Client Data
      |
      v
Local Training
      |
      v
Gradient Clipping
      |
      v
Noise Injection
      |
      v
Private Model Update
      |
      v
Global Aggregation
      |
      v
Updated Global Model
```

---

## Deep Learning Model

A Convolutional Neural Network (CNN) is used for intrusion detection.

### Architecture

```text
Input Layer
      |
Conv1D Layer
      |
Max Pooling
      |
Conv1D Layer
      |
Max Pooling
      |
Flatten Layer
      |
Dense Layer
      |
Output Layer
```

---

## Federated Learning Process

1. Data is distributed among multiple clients.
2. Each client trains its local model.
3. Differential Privacy is applied to local updates.
4. Private updates are sent to the server.
5. The server performs aggregation.
6. The global model is updated.
7. The process repeats for multiple rounds.

---

# Module 2: Zero-Day Attack Detection Framework

## Objective

Traditional IDS systems perform well on known attacks but struggle with previously unseen attacks.

This module introduces a Zero-Day Attack Detection mechanism capable of identifying anomalous behavior that was not present during training.

---

## Feature Selection Strategy

Multiple client perspectives are simulated using different feature selection techniques.

### Client 1

Chi-Square Feature Selection

### Client 2

Random Forest Feature Importance

### Client 3

Support Vector Machine (SVM) Feature Selection

### Client 4

Principal Component Analysis (PCA)

---

## Autoencoder-Based Anomaly Detection

An Autoencoder learns the patterns of normal network traffic.

### Working Principle

- Normal traffic is reconstructed accurately.
- Unknown attacks produce higher reconstruction errors.
- Reconstruction error is used as an anomaly score.

### Autoencoder Architecture

```text
Input Layer
      |
Dense Layer (128)
      |
Dense Layer (64)
      |
Latent Space
      |
Dense Layer (64)
      |
Dense Layer (128)
      |
Output Layer
```

---

## XGBoost Classification

XGBoost is used for attack classification.

Advantages:

- High accuracy
- Robust performance
- Handles class imbalance effectively
- Fast training

---

## Fusion-Based Detection

Predictions from multiple models are combined.

Inputs include:

- Autoencoder anomaly score
- XGBoost predictions
- Client-level predictions
- Malware detection outputs

The fusion mechanism generates the final threat decision.

---

## Zero-Day Detection Process

```text
Network Traffic
        |
        v
Feature Extraction
        |
        v
Autoencoder
        |
        v
Reconstruction Error
        |
        v
Anomaly Detection
        |
        v
Fusion Engine
        |
        v
Zero-Day Alert
```

---

# Performance Evaluation

The framework is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC Score
- Confusion Matrix
- False Positive Rate (FPR)
- Detection Rate

---

# Technologies Used

## Programming Language

- Python

## Deep Learning

- TensorFlow
- Keras
- PyTorch

## Machine Learning

- Scikit-Learn
- XGBoost

## Privacy Framework

- Opacus

## Data Processing

- Pandas
- NumPy

## Visualization

- Matplotlib
- Seaborn

---

# Repository Structure

```text
FL-IDS/
│
├── FL_IDS.ipynb
│   
├── Minor_Project_end_sem.ipynb

└── README.md
```

---

# Applications

- Enterprise Network Security
- Cloud Security
- IoT Security Monitoring
- Cyber Threat Intelligence
- Privacy-Preserving Analytics
- Security Operations Centers (SOC)

---

# Future Enhancements

- Flower-based Federated Learning
- TensorFlow Federated Integration
- Real-Time Packet Monitoring
- Explainable AI (XAI)
- Adaptive Privacy Budgeting
- Blockchain-Based Federated Aggregation
- Online Learning for Emerging Threats

---

# Research Contributions

This project demonstrates the integration of:

- Federated Learning
- Differential Privacy
- Deep Learning
- Machine Learning
- Zero-Day Attack Detection

to create a scalable, privacy-preserving, and intelligent cybersecurity framework.

---

# Advanced-Persistent-Threat-Detection-Using-Temporal-Graph-Neural-Networks
This project presents an advanced machine learning solution to detect Advanced Persistent Threats (APTs) using Temporal Graph Neural Networks (GNNs). Using the DAPT 2020 dataset, which contains network flow records captured during simulated attack scenarios, the system learns temporal patterns of malicious behaviors.

This repository contains code and experiments for detecting Advanced Persistent Threats (APTs) using Temporal Graph Neural Networks. The model captures time-evolving relationships between hosts and network activities to classify malicious stages with higher precision.

## Dataset

**Source:** [Kaggle - DAPT 2020](https://www.kaggle.com/datasets/sowmyamyneni/dapt2020)

### Data Includes:
- Timestamped bidirectional flows
- Source & destination IPs
- Protocol, port, byte, and packet counts
- Ground truth: `Activity` (e.g. Scan, Injection, Exfiltration), `Stage` (Reconnaissance, Lateral Movement, etc.)

##  Model Overview

- **Temporal Graph Construction**:
  - Nodes: Host IPs
  - Edges: Flows between hosts
  - Edge Features: Time delta, packet size, flow duration
- **Temporal GNN Architecture**:
  - GCN or GAT with time-aware edge encoding
  - Node/Edge classification layers for attack type & stage

##  Key Features

-  Time-aware modeling of flow sequences
-  Classifies both attack **activity** and **stage**
-  Handles missing and infinite values robustly
-  Visualizes APT attack patterns over time

## Visualisation 
#Apt attack detection graph

![image](https://github.com/user-attachments/assets/086ad661-ed07-482f-b8d4-3127c245e9da)

# Compare predicted vs. ground truth on test nodes only
![image](https://github.com/user-attachments/assets/295cdd5e-0f4d-4d0a-8861-ec5569c99cdd)


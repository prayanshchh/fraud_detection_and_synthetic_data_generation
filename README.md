# Fraud Detection and Synthetic Data Generation  

This repository contains the codebase for two key components:  
1. **Fraud Detection using Random Forest**  
2. **Synthetic Data Generation using SDV (Synthetic Data Vault)**  

These components are designed to facilitate secure and scalable fraud detection while enabling the generation of high-quality synthetic datasets for testing and model training purposes.  

---

## Table of Contents  
- [Overview](#overview)  
- [Fraud Detection](#fraud-detection)  
  - [Features](#features)  
  - [Implementation Details](#implementation-details)  
- [Synthetic Data Generation](#synthetic-data-generation)  
  - [Features](#features-1)  
  - [Implementation Details](#implementation-details-1)  
- [Setup Instructions](#setup-instructions)  
- [Usage](#usage)  
- [Contributing](#contributing)  
- [License](#license)  

---

## Overview  
This project aims to:  
1. Detect fraudulent transactions using a machine learning approach based on Random Forest.  
2. Generate synthetic datasets for model development and testing using SDV's `GaussianCopulaSynthesizer`.  

The repository is in its initial stages and is a work-in-progress to support hackathon development.  

---

## Fraud Detection  

### Features  
- **Real-Time Risk Scoring:** Assigns a risk score to transactions using `predict_proba` from Random Forest.  
- **Flexible Risk Categorization:** Transactions are categorized as low, medium, or high risk based on thresholds.  
- **Feature Importance:** Identifies and leverages key transaction attributes for fraud prediction.  

### Implementation Details  
- **Model:** Random Forest Classifier.  
- **Input Features:**  
  - Transaction type  
  - Flagged status  
  - Normalized transaction amount  
  - Origin and destination transaction patterns  
- **Output:** Probabilistic risk scores indicating likelihood of fraud.  

---

## Synthetic Data Generation  

### Features  
- **Realistic Data Patterns:** Captures statistical properties of real datasets to generate high-quality synthetic data.  
- **Scalability:** Handles small to large datasets efficiently.  
- **Privacy Protection:** Enables model testing without exposing sensitive data.  

### Implementation Details  
- **Tool Used:** SDV Library.  
- **Synthesizer:** `GaussianCopulaSynthesizer` for single-table data synthesis.  
- **Steps:**  
  1. Load real data from CSV files.  
  2. Fit the synthesizer to learn data patterns.  
  3. Generate synthetic data for further use.  

---

## Setup Instructions  

1. **Clone the Repository:**  
   ```bash  
   git clone https://github.com/yourusername/repo-name.git  
   cd repo-name  

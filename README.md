# 🚰 Reservoir Risk Prediction - Telangana, India

This project leverages historical reservoir data from 24 key reservoirs across Telangana to detect patterns of **water stress**, **drought conditions**, and **flood risk**. It provides real-time **classification**, **monitoring**, and **alerts** for decision-makers to respond effectively.

---

## 📌 Objectives

- Detect patterns of **drought** and **water stress**
- Classify reservoirs into **risk categories**
- Provide **real-time predictions** and **alerts**
- Enable **visual monitoring** via dashboards and a **Streamlit UI**

---

## 🧠 Models Overview

### ✅ Model 1: Basic Drought Classifier

| Component | Details |
|----------|---------|
| **Input** | Raw monthly reservoir data (24 `.csv` files) |
| **Process** | Data cleaning → Feature engineering → Binary classification |
| **Model** | `RandomForestClassifier` |
| **Output** | `is_drought` label + `cleaned_reservoir_dataset.csv` |
| **Purpose** | Establish foundational drought detection logic |

---

### 🔥 Model 2: Multiclass Risk Classifier + Alert System

| Component | Details |
|----------|---------|
| **Input** | Cleaned dataset with rainfall and flow indicators |
| **Model** | Multiclass `RandomForestClassifier` with label encoding |
| **Categories** | `No Risk`, `Caution`, `Water Stress`, `High Risk`, `Severe Risk`, `Probable chances of Flood` |
| **Output** | Real-time classification and alert generation |
| **Interface** | Streamlit App for interactive predictions |
| **Email Alerts** | Automated alerts for **Severe Risk** and **Flood Probability** |

---

## ⚙️ Features Used

- `storage_percent`
- `net_flow`
- `flow_ratio`
- `net_flow_per_capacity`
- `Avg_monthly_Rainfall`
- `Normal Rainfall`
- `gross_storage`
- `level_in_feet_present`

---

🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/reservoir-risk-prediction.git
cd reservoir-risk-prediction
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit App
```bash
streamlit run streamlit_ai_agent.py
```

## Once the app is running:

 Upload the model logic file: model_2_streamlit_ready.py
 
 
 Upload the dataset: cleaned_reservoir_dataset_with_rainfall.csv


## 📬 Email Alert System

The system automatically sends email alerts when any reservoir is flagged under:
 1. Severe Risk
 2. Probable chances of a Flood


## ✉️ Alert Email Includes:

 1. Reservoir Name
 2. District
 3. Risk Category
All formatted using a clean ASCII table for readability

## 📊 Dashboards (Power BI)

This project includes rich visual dashboards for analysis:
 1. Exploratory Dashboard: Visualizes rainfall patterns, inflow/outflow behavior, and storage trends
 2. Risk Dashboard: District-wise risk categories and classification results
Developed using Microsoft Power BI (.pbix files).



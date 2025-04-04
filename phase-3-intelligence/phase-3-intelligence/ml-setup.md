# 🤖 ML Setup – Product Recommendations

This document outlines how to configure Azure Machine Learning for generating personalized product suggestions.

---

## 🔧 Workspace Setup

1. Go to [Azure Portal](https://portal.azure.com)
2. Search for **Machine Learning** → Click **+ Create**
3. Use the following configuration:
   - **Name:** `CashierlessML`
   - **Region:** Same as your other resources
   - **Compute:** Basic CPU Cluster (low cost)
   - Enable notebooks

---

## 📁 Data Prep

1. Open the Azure ML Studio
2. Create a new **Dataset** from Dataverse export or Azure SQL:
   - **Table:** `Feedback`
   - Include: `User`, `Rating`, `Category`
3. Clean and group feedback data by user

---

## 🧠 Model Training

Use AutoML or custom training (Python notebook) to train:

- **Goal:** Predict top 3 categories per user
- **Algorithm (suggested):** Classification or Multi-label model
- **Output Table:** `AIRecommendations`

---

## 🚀 Deployment

1. Register trained model  
2. Deploy as real-time endpoint  
3. Connect to Power Apps using **Power Platform Connector for Azure ML**

---

✅ **Next Step**  
Create `iot-setup.md` to simulate product pickup detection using Azure IoT Hub.

# 🛍️ Cashierless Store App

An end-to-end **Cashierless Store System** built using **Power Apps**, **Azure**, **AI**, **IoT**, and **SharePoint**.  
Customers walk in, scan a QR, pick products, and get auto-charged — no cashier needed!

---

## 🚀 Tech Stack

| Component        | Technology Used                          |
|------------------|------------------------------------------|
| App Platform     | Power Apps (Canvas & Model-Driven)       |
| Database         | Dataverse, Azure SQL                     |
| AI/ML            | Azure Machine Learning                   |
| IoT Simulation   | Raspberry Pi (mock) + Azure IoT Hub      |
| Document Storage | SharePoint Online                        |
| Workflow Engine  | Power Automate                           |
| Reporting        | Power BI                                 |
| Version Control  | GitHub                                   |

---

## 📦 Features

### 👥 Customer App (Canvas)
- Scan QR code to enter
- AI-driven product recommendations
- Feedback submission (text, rating, image)

### 🛠️ Admin App (Model-Driven)
- Manage transactions and feedback
- Embedded Power BI dashboards
- Manual override for billing issues

### 🧠 AI & Sensors
- Personalized suggestions from Azure ML
- Mock shelf sensors (via Raspberry Pi)
- Auto-detect item pickup events

### 🔗 SharePoint Integration
- Store customer images and reports
- Power Automate sends low-rating feedback to SharePoint list
- Weekly PDF exports from Power BI to SharePoint library

---

## 📁 Project Folder Structure

```bash
cashierless-store-app/
│
├── phase-1-setup/                # Azure, SharePoint, and Dataverse setup
│   ├── environment-setup.md
│   └── sharepoint-setup.md
│
├── phase-2-apps/                 # Power Apps
│   ├── customer-app/
│   │   ├── screens.md
│   │   └── controls-logic.md
│   └── admin-app/
│       ├── entities.md
│       └── dashboards.md
│
├── phase-3-ai/                   # Azure ML model + API
│   ├── model-training.ipynb
│   └── integration-steps.md
│
├── phase-4-iot/                  # Raspberry Pi + IoT Hub
│   └── sensor-mocking.md
│
├── phase-5-testing/
│   └── uat-checklist.md
│
├── phase-6-deployment/
│   └── rollout-plan.md
│
└── assets/                       # Screenshots, diagrams, sample data
    ├── app-screenshots/
    └── architecture-diagram.png

---

## 🗓️ Weekly Progress Plan

| Week | Focus Area                              |
|------|------------------------------------------|
| 1    | Azure setup + Dataverse + SharePoint     |
| 2    | Power Apps (Customer UI)                 |
| 3    | AI Model (Azure ML + API)                |
| 4    | Testing and feedback collection          |
| 5    | Pilot deployment + flow automation       |


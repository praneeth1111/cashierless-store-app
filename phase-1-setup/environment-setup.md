# ⚙️ Environment Setup Guide

This document helps you configure all backend services for the cashierless store project.

---

## ✅ Services to Set Up in Azure

### 1. Azure SQL Database
- **Purpose**: Store transactions and product info
- **Steps**:
  - Go to Azure Portal → SQL Databases → Create
  - Choose a resource group
  - Set DB name: `CashierlessStoreDB`
  - Server: Create new or use existing
  - Pricing: Start with Basic tier (Free)
  - Enable firewall access to your IP

### 2. Azure Machine Learning
- **Purpose**: Build recommendation model
- **Steps**:
  - Go to Azure Portal → Machine Learning → Create workspace
  - Name: `CashierlessMLWorkspace`
  - Enable notebooks
  - Set compute target (Basic CPU cluster for now)

### 3. Azure IoT Hub (Simulated for Raspberry Pi)
- **Purpose**: Connect simulated sensors
- **Steps**:
  - Azure Portal → IoT Hub → Create
  - Tier: Free (F1)
  - Device ID: `MockSensor1`
  - Use `az iot hub` CLI to simulate sensor data (or Python)

---

## 🗃️ Dataverse Setup (via Power Platform)

### Create a new solution:
- Name: `CashierlessStoreSolution`
- Environment: Default or new sandbox

### Tables to Add:
| Table         | Columns                                        |
|---------------|------------------------------------------------|
| Feedback      | Rating (Number), Comment (Text), Image (File) |
| Products      | Name, Category, Price                          |
| Transactions  | UserID, ProductID, Timestamp                   |

---

## 🔐 Permissions

- Go to Azure Portal → Subscriptions → Access control (IAM)
- Assign your Power Apps user:
  - Role: **Contributor**
  - Scope: Subscription or Resource Group

---

## ✅ Next Step

Move to `sharepoint-setup.md` for configuring the SharePoint site and Power Automate integrations.

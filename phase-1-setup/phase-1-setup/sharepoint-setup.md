# 🗂️ SharePoint Setup Guide

This file explains how SharePoint is used in the cashierless store project for document storage and integration with Power Platform.

---

## ✅ Use Cases for SharePoint

### 1. Document Library
- Store reports, user manuals, product PDFs
- Power BI exports can be auto-saved here weekly

### 2. Feedback Images
- Store customer-submitted photos from Power Apps
- Uploaded via Power Automate flows

### 3. Feedback Archive List
- Create a SharePoint List named `NegativeFeedback`
- Used by Power Automate to log low-rated reviews

---

## 🔧 Steps to Set Up

### 📁 Create a SharePoint Site:
- Go to [https://portal.office.com](https://portal.office.com)
- Choose **SharePoint** → Create site → Team Site
- Site Name: `CashierlessStoreSite`

---

### 📂 Create Document Library:
- Name: `StoreReports`
- Use this for uploading customer feedback images and reports

---

### 📋 Create a SharePoint List:
- Name: `NegativeFeedback`
- Columns:
  - Rating (Number)
  - Comment (Text)
  - SubmittedBy (Text)
  - ImageURL (Hyperlink)

---

## 🔗 Power Automate Integration

### Flow #1: Upload Photo to SharePoint
- **Trigger**: New feedback in Dataverse
- **Action 1**: Convert image to file
- **Action 2**: Upload to `StoreReports` library

### Flow #2: Archive Bad Feedback
- **Trigger**: When feedback rating < 3
- **Action**: Create item in `NegativeFeedback` SharePoint List

---

## 🔐 Permissions

- Make sure your Power Apps and Power Automate connections have:
  - **Edit access** to SharePoint site and list
  - Proper authentication (OAuth or service principal)

---

## ✅ Next Step

Move on to `phase-2-apps/customer-app/screens.md` to begin designing the user interface in Power Apps.

# 🗂️ Power Apps – Dataverse Tables

This file describes the Dataverse tables used in the cashierless store customer-facing Canvas App.

---

## 📝 Feedback

Stores customer feedback ratings, comments, and images.

| Column Name     | Data Type | Description                   |
|------------------|-----------|-------------------------------|
| Rating           | Number    | Star rating (1–5)             |
| Comments         | Text      | Optional customer input       |
| Image            | Image     | Photo uploaded from camera    |
| Submitted By     | Lookup    | Linked to User                |
| Submission Date  | DateTime  | Captured automatically        |

---

## 📦 Products

Product catalog displayed to users with category tags.

| Column Name     | Data Type | Description                   |
|------------------|-----------|-------------------------------|
| Product Name     | Text      | Name of the product           |
| Price            | Currency  | Sale price                    |
| Category         | Text      | For AI recommendation logic   |
| Image            | Image     | Product image                 |
| In Stock         | Boolean   | Inventory availability        |

---

---

## 🧠 AIRecommendations

Stores product category recommendations generated via Azure ML.

| Column Name | Data Type | Description                     |
|-------------|-----------|---------------------------------|
| UserEmail   | Text      | Email of the current user       |
| Categories  | Choice[]  | Suggested categories to display |

---

## 🛒 Cart (Local Collection)

Used to temporarily store selected products before checkout.

| Column Name | Data Type | Description                     |
|-------------|-----------|---------------------------------|
| ProductName | Text      | Name of product added to cart   |
| Price       | Currency  | Product price                   |
| Quantity    | Number    | Quantity selected by user       |


# 🗄️ Power Apps – Admin App Tables

This file documents the Dataverse tables used in the cashierless store admin app.

---

## 📦 Inventory

Stores all product stock, supplier details, and pricing.

| Column Name     | Data Type | Description                  |
|-----------------|-----------|------------------------------|
| Product Name     | Text      | Item name                    |
| SKU              | Text      | Unique Stock Keeping Unit    |
| Supplier         | Text      | Vendor/supplier name         |
| Quantity In Stock| Number    | Available units              |
| Price Per Unit   | Currency  | Cost per item                |
| Reorder Level    | Number    | Minimum stock alert level    |

---

## 👥 User Roles

Defines admin roles and access levels for the app.

| Column Name     | Data Type | Description                          |
|-----------------|-----------|--------------------------------------|
| User Name       | Text      | Admin's display name                 |
| Email           | Text      | Linked user email address            |
| Role            | Choice    | Admin / Supervisor / Store Manager   |
| Permissions     | MultiSelect | Access privileges (Edit, View, Delete) |

---


# 🛒 E-COMMERCE-DATABASE-TASK-3

This repository contains the schema and SQL scripts for an **E-Commerce Database System**.  
The database is designed to handle various e-commerce operations, including **user management, product catalog, orders, payments, categories**, and more.

---

## 📌 Features

- **Users**: Manage user details, including authentication and profiles.
- **Products**: Catalog of products with categories, prices, and inventory management.
- **Orders**: Track customer orders, including order status and payment details.
- **Payments**: Handle payment information, linked to orders.
- **Categories**: Organize products into categories for easy navigation.
- **Order Items**: Store detailed information about each item in an order.

---

## 🏗️ Database Schema

The database consists of the following key tables:

| Table Name       | Description |
|------------------|-------------|
| `users`          | Stores user information (name, email, password). |
| `products`       | Stores product details (name, price, category). |
| `orders`         | Stores customer order information (order date, status). |
| `order_items`    | Details of each item in an order. |
| `payments`       | Payment records linked to orders. |
| `categories`     | Product categories for classification. |

---

## 📊 Views & Summaries

The database includes the following views for analytics:

- **`user_order_summary`**: Total number of orders and total amount spent per user.
- **`product_sales_summary`**: Total quantity sold and total revenue per product.
- **`category_sales_summary`**: Total revenue and products sold per category.

---

## ⚡ Indexes for Performance

| Index Name                  | Description |
|-----------------------------|-------------|
| `idx_orders_user_id`        | Index on `user_id` in `orders` table. |
| `idx_order_items_order_id`  | Index on `order_id` in `order_items` table. |
| `idx_order_items_product_id`| Index on `product_id` in `order_items` table. |
| `idx_products_category_id`  | Index on `category_id` in `products` table. |
| `idx_payments_order_id`     | Index on `order_id` in `payments` table. |

---

## 🛡️ Error Handling & Data Integrity

- **SQL Constraints**:
  - `NOT NULL`
  - `FOREIGN KEY`
  - `UNIQUE`  
- Queries are written to handle:
  - Duplicate order prevention
  - Missing product references
  - Data consistency enforcement

---

## 🚀 Performance Considerations

- Indexing on frequently queried columns to improve query speed.
- **Database normalization** for data integrity.
- **Denormalization** for certain reporting queries.
- Regular **index maintenance** and **statistics updates** recommended.

---

## 🛠️ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/E-COMMERCE-DATABASE-TASK-3.git
   cd E-COMMERCE-DATABASE-TASK-3

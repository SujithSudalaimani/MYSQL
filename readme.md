 E-commerce Database Project

This project is a simple e-commerce database system built using MySQL. It includes a normalized database schema with tables for `customers`, `orders`, `products`, and `order_items`. The project demonstrates key SQL concepts including data relationships, joins, aggregation, and normalization.


Database Tables
 `customers`
- `id` (PK)
- `name`
- `email`
- `address`

`products`
- `id` (PK)
- `name`
- `price`
- `description`
- `discount`

`orders`
- `id` (PK)
- `customer_id` (FK)
- `order_date`

`order_items`
- `id` (PK)
- `order_id` (FK)
- `product_id` (FK)
- `quantity`

Queries

- Retrieve all customers who have placed an order in the last 30 days.
- Get the total amount of all orders placed by each customer.
- Update the price of Product C to 45.00.
- Add a new column discount to the products table.
- Retrieve the top 3 products with the highest price.
- Get the names of customers who have ordered Product A.
- Join the orders and customers tables to retrieve the customer's name and order date for each order. 
- Retrieve the orders with a total amount greater than 150.00.
- Normalize the database by creating a separate table for order items and updating the orders table to reference the order_items table.
- Retrieve the average total of all orders.




Notes

- The database is normalized: `order_items` replaces `total_amount` in `orders`.
- Order totals are calculated using dynamic `JOIN` queries, not stored.
- Discounts are supported via an optional column in `products`.


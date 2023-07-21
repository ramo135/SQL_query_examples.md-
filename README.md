# SQL_query_examples.md

1. **Basic Data Retrieval:**
   ```sql
   SELECT first_name, last_name, email
   FROM customers
   WHERE country = 'USA';

2. **Aggregation:**
   ```sql
   SELECT category, COUNT(*) AS total_products
   FROM products
   GROUP BY category;

3. **Joins:**
   ```sql
   SELECT orders.order_id, customers.first_name, customers.last_name
   FROM orders
   INNER JOIN customers ON orders.customer_id = customers.customer_id;
 
4. **Filtering with Conditions**
   ```sql
   SELECT product_name, unit_price
   FROM products
   WHERE unit_price > 50 AND category = 'Electronics';

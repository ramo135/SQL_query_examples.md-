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

5. **Subqueries**
   ```sql
   SELECT product_name
   FROM products
   WHERE category IN (SELECT category FROM popular_categories);

6. **Sorting and Limiting Results**
   ```sql
   SELECT product_name, unit_price
   FROM products
   ORDER BY unit_price DESC
   LIMIT 10;

7. **Updating Data**
   ```sql
   UPDATE customers
   SET status = 'Premium'
   WHERE total_purchase_amount > 1000;

8. **Multiple Joins**
   ```sql
   SELECT orders.order_id, customers.first_name, customers.last_name, products.product_name
   FROM orders
   INNER JOIN customers ON orders.customer_id = customers.customer_id
   INNER JOIN order_details ON orders.order_id = order_details.order_id
   INNER JOIN products ON order_details.product_id = products.product_id;

9. **Date Manipulation**
    ```sql
    SELECT customer_id, order_date
    FROM orders
    WHERE DATE(order_date) >= '2023-01-01' AND DATE(order_date) <= '2023-06-30';


   

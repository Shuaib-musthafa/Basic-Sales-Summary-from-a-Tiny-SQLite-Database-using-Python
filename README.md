# 🛒 Task 7 - Sales Summary using SQLite and Python

## 📌 Objective
This task demonstrates how to extract a basic sales summary from an SQLite database using Python, SQL, and data visualization tools.

We:
- Created a sample `sales_data.db` SQLite database.
- Queried it using SQL to calculate **total quantity sold** and **total revenue** by product.
- Displayed the output using `print()` and visualized it with `matplotlib`.

---

## 🛠 Tools & Technologies
- Python
- SQLite (`sqlite3`)
- Pandas
- Matplotlib

---

## 📂 Project Files
- `SQLite.ipynb`: Jupyter notebook containing the complete code (DB creation, SQL query, and visualization).
- `sales_data.db`: SQLite database file (generated during execution).
- `sales_chart.png`: Bar chart showing revenue by product (saved automatically).
- `README.md`: This file.

---

## 📊 Summary of Work

### 1. Create the Database
We created a `sales` table and populated it with **100+ randomized product entries** including:
- Pen, Notebook, Eraser, Pencil, Marker, Scale, Highlighter, Stapler

### 2. SQL Query Used:
```sql
SELECT 
    product, 
    SUM(quantity) AS total_quantity, 
    ROUND(SUM(quantity * price), 2) AS total_revenue
FROM sales
GROUP BY product
ORDER BY total_revenue DESC
```

---

### 3. Output Sample:
| product     | total_quantity | total_revenue |
|-------------|----------------|----------------|
| Notebook    | 150            | 450.00         |
| Pen         | 200            | 300.00         |
| ...         | ...            | ...            |
### 4. Visualization
A bar chart was created using matplotlib to visualize total revenue per product.

Chart saved as sales_chart.png.

📷 Screenshot
![image](https://github.com/user-attachments/assets/94dec464-e7ea-4a41-8515-0020b7760619)


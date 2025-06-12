# SQLite and python
Create a small SQLite database file (sales_data.db) with just one sales table  aand Runs 1–2 SQL queries, Displays output using print and basic matplotlib bar chart

Great! Here's a simple and clean Python script (works in Jupyter Notebook too) that:
Connected  to  sales_data.db
Runs a basic SQL query to get total quantity and revenue per product
Displays the result in the terminal
Plots a bar chart using matplotlib

import sqlite3
import pandas as pd
import matplotlib.pyplot as plt
conn = sqlite3.connect('sales_data.db')
# Create a cursor object
cursor = conn.cursor()
cursor.execute("DROP TABLE IF EXISTS sales")
cursor.execute('''
CREATE TABLE IF NOT EXISTS sales (
    order_id INTEGER PRIMARY KEY,
    order_date TEXT,
    customer_name TEXT,
    product TEXT,
    quantity INTEGER,
    price_per_unit REAL,
    total_amount REAL
)
''')
above  are basic after that we can modify
.
.
.
.
.

** Basic Sales Summary from SQLite Database **

🎯 Objective

  Create a small SQLite database with sales data, run SQL queries to calculate total quantities and revenues by product, and visualize results using a bar chart.

🛠 Tools

  • Python 3
  • sqlite3 (built-in) – database operations
  • pandas – data handling
  • matplotlib – chart plotting

🔄 Workflow

  1. Connect to SQLite – Creates/opens sales_data.db.
  2. Create Table – sales table with product, quantity, price.
  3. Insert Sample Data – Multiple product sales records via executemany().

  4. Run SQL Query –

       SELECT product, SUM(quantity) AS total_qty, SUM(quantity * price) AS revenue
       FROM sales
       GROUP BY product;

  5. Display Results – Load into pandas DataFrame & print table.
  6. Plot Chart – Bar chart of revenue by product, saved as sales_chart.png.


▶ How to Run
    
  pip install pandas matplotlib
  python sales_summary.py


📈 Output

  • Terminal: Sales summary table with total quantities & revenues.
  • File: sales_chart.png – bar chart of revenue by product.

⚠ Note

  • To avoid duplicate rows when re-running, clear the table first:
   
   cursor.execute("DELETE FROM sales")

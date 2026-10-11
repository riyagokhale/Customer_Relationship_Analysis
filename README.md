# Customer_Relationship_Analysis
Data Analytics Project with Python, SQL and Power BI
# Customer Behavior Analysis with Python, SQL and Power BI

An end-to-end analysis of retail customer shopping data. I took a raw dataset, cleaned it in Python, loaded it into a SQL database to answer business questions, built an interactive Power BI dashboard on top of it, and wrote up the findings as a report and presentation.

I built this to practice the full analyst workflow in one place instead of treating cleaning, querying and visualization as separate exercises.

## The problem

A retail business wants to understand who its customers are and what drives their purchases. The questions I set out to answer:

- Which customer segments bring in the most revenue?
- How do loyalty and repeat purchase behavior differ across customers?
- What factors (category, season, payment method, discounts, shipping, and so on) are linked to higher spending?
- What should the business do differently based on these patterns?

## Tools used

| Stage | Tool |
|---|---|
| Cleaning, exploration, feature creation | Python (pandas, NumPy, Jupyter) |
| Database and analysis | SQL (MySQL / PostgreSQL / SQL Server) |
| Dashboard | Power BI |
| Reporting | Written report and slide presentation |

## How the project is organized

```
├── Customer_Shopping_Behavior_Analysis.ipynb   # Python: import, EDA, cleaning, database load
├── customer_behavior_sql_queries.sql           # SQL: business questions and answers
├── customer_behavior_dashboard.pbix            # Power BI dashboard
└── README.md
```

## Workflow

### 1. Data preparation and exploration (Python)

I started in a Jupyter notebook by loading the raw file and getting a feel for it: column types, row counts, summary statistics, and distributions.

From there I cleaned the data:

- Checked for missing values and decided how to handle each column rather than dropping rows blindly
- Looked for duplicates and inconsistent formatting
- Standardized column names and data types so they behave well in SQL
- Created a few extra columns to make segmentation easier later, such as grouped categories

Once the data was in good shape, I connected the notebook to a SQL database and loaded the cleaned table straight from Python.

### 2. Business analysis (SQL)

With the data in a database, I wrote queries to answer the questions above. The queries in `customer_behavior_sql_queries.sql` cover things like:

- Revenue and order counts by customer segment
- Comparing loyal, returning and new customers
- Spending patterns by product category, season and payment method
- The effect of discounts and promotions on purchase behavior
- Ranking and filtering to find top-performing groups

I used aggregations, grouping, CTEs and window functions where they made the query clearer, and tried to keep each query focused on one question.

### 3. Dashboard (Power BI)

I connected Power BI to the database and built a dashboard that lets someone explore the results without touching SQL. It includes headline KPIs, breakdowns by segment and category, and filters so a viewer can slice the data themselves.

The aim was a dashboard a non-technical stakeholder could open and understand within a minute or two.

### 4. Report and presentation

Finally, I summarized the work in a short report and a slide deck: the question, the approach, the key findings, and concrete recommendations for the business.

## Key findings

*Add your own results here once you're happy with the numbers. For example: the segment with the highest revenue, the loyalty pattern you found, and one or two recommendations that came out of it.*

## Running it yourself

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```
2. Install the Python dependencies (pandas, NumPy, SQLAlchemy, and a driver for your database, plus Jupyter).
3. Create an empty database in MySQL, PostgreSQL or SQL Server.
4. Open the notebook, update the connection string with your own credentials, and run it top to bottom. This cleans the data and loads it into your database.
5. Run the queries in `customer_behavior_sql_queries.sql` against that database.
6. Open `customer_behavior_dashboard.pbix` in Power BI and point the data source at your database.

## What I learned

- Cleaning decisions matter. Every choice about missing values or outliers changes the numbers downstream.
- Doing the analysis in SQL, rather than only in pandas, forced me to think about how the data is structured and how a team would really query it.
- A dashboard is only useful if it answers a question someone actually has.



## About me

I'm Riya Gokhale, and I'm building my skills in data analytics. This project is part of my portfolio.

- LinkedIn: https://www.linkedin.com/in/riya-gokhale-b559b0233


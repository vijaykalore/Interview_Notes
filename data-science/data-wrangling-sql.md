# Data Wrangling and SQL for Data Science

Data wrangling, also known as data munging, is the process of transforming and mapping raw data into a more usable format. This is a crucial step in the data science workflow, as it ensures that the data is clean, consistent, and ready for analysis. SQL (Structured Query Language) is a powerful tool used for managing and manipulating relational databases, making it essential for data wrangling tasks.

## Key Concepts in Data Wrangling

### 1. Data Cleaning
- **Handling Missing Values**: Techniques include imputation, deletion, and using algorithms that support missing values.
- **Removing Duplicates**: Identifying and eliminating duplicate records to ensure data integrity.
- **Outlier Detection**: Methods to identify and handle outliers, such as Z-scores and IQR.

### 2. Data Transformation
- **Normalization and Standardization**: Scaling data to a common range or distribution.
- **Encoding Categorical Variables**: Techniques like one-hot encoding and label encoding to convert categorical data into numerical format.
- **Feature Engineering**: Creating new features from existing data to improve model performance.

### 3. Data Integration
- **Merging Datasets**: Combining multiple datasets using SQL JOIN operations (INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL OUTER JOIN).
- **Data Aggregation**: Using SQL GROUP BY to summarize data and calculate metrics like averages, sums, and counts.

## SQL for Data Wrangling

### Basic SQL Commands
- **SELECT**: Retrieve data from one or more tables.
- **WHERE**: Filter records based on specific conditions.
- **ORDER BY**: Sort the result set by one or more columns.
- **GROUP BY**: Group rows that have the same values in specified columns into summary rows.

### Advanced SQL Techniques
- **Subqueries**: Using a query within another query to filter or aggregate data.
- **Common Table Expressions (CTEs)**: Temporary result sets that can be referenced within a SELECT, INSERT, UPDATE, or DELETE statement.
- **Window Functions**: Performing calculations across a set of table rows related to the current row.

### Example SQL Queries
```sql
-- Selecting specific columns from a table
SELECT name, age, salary
FROM employees
WHERE department = 'Sales';

-- Joining two tables
SELECT e.name, d.department_name
FROM employees e
JOIN departments d ON e.department_id = d.id;

-- Aggregating data
SELECT department_id, AVG(salary) as average_salary
FROM employees
GROUP BY department_id;
```

## Best Practices in Data Wrangling
- Always keep a copy of the original dataset.
- Document the data wrangling process for reproducibility.
- Use version control for scripts and datasets.
- Validate the results of data wrangling steps to ensure accuracy.

## Conclusion
Data wrangling is a foundational skill for data scientists and ML engineers. Mastery of SQL and data manipulation techniques is essential for preparing data for analysis and modeling. Understanding these concepts will not only enhance your technical skills but also improve your performance in data-driven roles.
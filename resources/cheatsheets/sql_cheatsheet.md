# SQL Cheatsheet para entrevistas de datos

## Window Functions

```sql
-- Rank dentro de grupos
SELECT name, dept, salary,
  ROW_NUMBER() OVER (PARTITION BY dept ORDER BY salary DESC) AS rn,
  RANK()       OVER (PARTITION BY dept ORDER BY salary DESC) AS rnk,
  DENSE_RANK() OVER (PARTITION BY dept ORDER BY salary DESC) AS dense_rnk
FROM employees;

-- Running total
SELECT date, amount,
  SUM(amount) OVER (ORDER BY date) AS running_total
FROM sales;

-- Valor anterior y siguiente
SELECT date, value,
  LAG(value)  OVER (ORDER BY date) AS prev_value,
  LEAD(value) OVER (ORDER BY date) AS next_value
FROM metrics;
```

## CTEs

```sql
WITH high_earners AS (
  SELECT * FROM employees WHERE salary > 100000
)
SELECT dept, COUNT(*) FROM high_earners GROUP BY dept;
```

## Patrones frecuentes en entrevistas

```sql
-- Second highest salary
SELECT MAX(salary) FROM employees
WHERE salary < (SELECT MAX(salary) FROM employees);

-- Duplicados
SELECT email, COUNT(*) FROM users
GROUP BY email HAVING COUNT(*) > 1;

-- Employees earning more than manager
SELECT e.name FROM employees e
JOIN employees m ON e.manager_id = m.id
WHERE e.salary > m.salary;
```

# SQL Queries and Joins

**Key points / formula:** SELECT ... FROM ... WHERE ... GROUP BY ... HAVING ... ORDER BY. INNER JOIN returns only matching rows in both tables; LEFT JOIN returns all rows from the left table plus matches (NULLs where no match); RIGHT JOIN is the mirror of LEFT; FULL JOIN returns all rows from both, matched where possible.

**When it's asked (pattern cue):** "Write a query to find the second-highest salary," "difference between WHERE and HAVING," or any live query-writing exercise.

**Worked micro-example:** Second-highest salary.
```sql
SELECT MAX(salary) FROM Employees
WHERE salary < (SELECT MAX(salary) FROM Employees);
```

**Common gotcha / trick:** Using WHERE to filter on an aggregate (e.g. `WHERE COUNT(*) > 1`) instead of HAVING (WHERE filters rows before grouping, HAVING filters after); forgetting that a LEFT JOIN with a WHERE clause on the right table's column can accidentally behave like an INNER JOIN if NULLs aren't handled.

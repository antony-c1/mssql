# NULL LAST

In SQL Server, you can use the `ORDER BY` clause to sort null values either first or last in the result set. To list null values last, you can use the `CASE` expression within the `ORDER BY` clause. Here's how you can do it:

```sql
SELECT column1, column2, ...
FROM your_table
ORDER BY CASE WHEN your_column IS NULL THEN 1 ELSE 0 END, your_column;
```

Explanation:
- The `CASE` expression checks if the column value is `NULL`. If it is `NULL`, it assigns a value of 1, otherwise 0.
- The `ORDER BY` clause sorts the rows based on the result of the `CASE` expression, with rows having `NULL` values sorted to the end of the result set.

Replace `your_table` with the name of your table and `your_column` with the column you want to sort. This query will list rows with null values in the specified column at the bottom of the result set.

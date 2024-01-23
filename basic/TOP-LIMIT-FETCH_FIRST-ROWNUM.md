# TOP, LIMIT, FETCH FIRST or ROWNUM

SQL Server uses the `TOP` keyword to limit the number of rows returned by a query. The syntax for `TOP` is as follows:

```sql
SELECT TOP (expression) column1, column2, ...
FROM table
WHERE condition;
```

Here, `expression` specifies the number of rows to be returned. It could be a constant, variable, or an expression that evaluates to an integer.

For example, if you want to retrieve the top 10 rows from a table called `YourTable`, you can use:

```sql
SELECT TOP 10 *
FROM YourTable;
```

Alternatively, if you want to use an offset and fetch a specific number of rows after skipping the initial rows, you can use `OFFSET` and `FETCH` clauses in combination with the `ORDER BY` clause. This is commonly used for pagination.

Here's an example:

```sql
SELECT column1, column2, ...
FROM YourTable
ORDER BY YourOrderingColumn
OFFSET 10 ROWS -- Skip the first 10 rows
FETCH NEXT 10 ROWS ONLY; -- Fetch the next 10 rows
```

In this example, `YourOrderingColumn` is the column based on which you want to order the result set.

It's important to note that the `OFFSET` and `FETCH` clauses were introduced in SQL Server 2012, so if you are using an older version, you might need to use other methods like `ROW_NUMBER()` for achieving similar results.

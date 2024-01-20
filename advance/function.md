# FUNCTION

In Microsoft SQL Server (MSSQL), a function is a precompiled and reusable SQL code block that performs a specific operation and returns a single value or a table result set. Functions can be used to encapsulate logic, promote code reuse, and simplify complex queries. There are two main types of functions in MSSQL: scalar functions and table-valued functions.

### Scalar Functions:

Scalar functions return a single scalar value (a single data value) based on the input parameters provided. Scalar functions can be used wherever an expression is allowed in a SQL query.

Here's a simple example of a scalar function that adds two numbers:

```sql
CREATE FUNCTION dbo.AddNumbers
(
    @Number1 INT,
    @Number2 INT
)
RETURNS INT
AS
BEGIN
    RETURN @Number1 + @Number2;
END;
```

You can then use this function in a query like this:

```sql
SELECT dbo.AddNumbers(5, 7) AS Result; -- Returns 12
```

### Table-Valued Functions:

Table-valued functions return a table result set, which can be used like a regular table in a SQL query.

Here's an example of a table-valued function that retrieves employees with a salary higher than a specified threshold:

```sql
CREATE FUNCTION dbo.GetHighSalaryEmployees
(
    @SalaryThreshold INT
)
RETURNS TABLE
AS
RETURN
(
    SELECT *
    FROM Employees
    WHERE Salary > @SalaryThreshold
);
```

You can use this table-valued function in a query like this:

```sql
SELECT *
FROM dbo.GetHighSalaryEmployees(50000);
```

### System Functions:

SQL Server also provides a variety of built-in system functions that perform specific tasks. These include functions for string manipulation, date and time operations, mathematical calculations, and more.

For example, the `GETDATE()` function returns the current date and time:

```sql
SELECT GETDATE() AS CurrentDateTime;
```

Functions in MSSQL can be deterministic or nondeterministic. Deterministic functions always return the same result for the same input, while nondeterministic functions may return different results for the same input at different times.

These are just basic examples, and functions in SQL Server can become more complex, involving conditional logic, loops, and other programming constructs. Functions provide a powerful way to modularize and reuse code within SQL Server databases.

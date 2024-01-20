# Store Procedure

In Microsoft SQL Server, a stored procedure is a precompiled collection of one or more Transact-SQL statements or batches that are stored as a single object in the database. Stored procedures can be called to perform a specific task or a set of tasks. Here is a basic syntax for creating a stored procedure:

```sql
CREATE PROCEDURE ProcedureName
    @Parameter1 DataType1,
    @Parameter2 DataType2
AS
BEGIN
    -- SQL statements to implement the procedure logic
END;
```

Here's a more detailed explanation:

- `ProcedureName`: The name of the stored procedure.
- `@Parameter1`, `@Parameter2`: Input parameters for the stored procedure, each with its data type.
- `AS`: The keyword that begins the body of the stored procedure.
- `BEGIN` and `END`: Delimiters that enclose the body of the stored procedure.
- The body of the stored procedure consists of one or more Transact-SQL statements that implement the logic of the procedure.

Here's an example of a simple stored procedure that retrieves employee details based on an employee ID:

```sql
CREATE PROCEDURE GetEmployeeDetails
    @EmployeeID INT
AS
BEGIN
    SELECT *
    FROM Employees
    WHERE EmployeeID = @EmployeeID;
END;
```

You can execute the stored procedure like this:

```sql
EXEC GetEmployeeDetails @EmployeeID = 101;
```

Stored procedures can also have output parameters, return values, and can execute other stored procedures or SQL statements. They provide a way to encapsulate and reuse logic within the database. Additionally, stored procedures can enhance performance by reducing the need to send multiple queries over the network.

Remember to adapt the stored procedure based on your specific requirements and the structure of your database.

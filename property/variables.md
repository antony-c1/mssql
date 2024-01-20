# Variables

In Microsoft SQL Server (MSSQL), you can declare and use variables within a batch or a stored procedure. Here's how you can declare a variable and use it:

### Declaration of a Variable:

To declare a variable, you use the `DECLARE` statement. The general syntax is as follows:

```sql
DECLARE @VariableName DataType;
```

- `@VariableName`: The name of the variable, preceded by the '@' symbol.
- `DataType`: The data type of the variable, such as `INT`, `VARCHAR`, `DATETIME`, etc.

### Assignment of a Value to a Variable:

After declaring a variable, you can assign a value to it using the `SET` statement or as part of the `DECLARE` statement. Here are examples for both cases:

#### Using SET:

```sql
DECLARE @MyVariable INT;
SET @MyVariable = 42;
```

#### Using DECLARE and Initialization:

```sql
DECLARE @MyVariable INT = 42;
```

### Using Variables in Queries:

Once a variable is declared and assigned a value, you can use it in your queries. Here's an example:

```sql
DECLARE @UserName VARCHAR(50);
SET @UserName = 'John';

SELECT *
FROM Users
WHERE Name = @UserName;
```

In this example, the variable `@UserName` is declared as a `VARCHAR` and is then used in the `SELECT` statement to filter the rows in the `Users` table.

### Example of a Simple Stored Procedure:

Here's an example of a simple stored procedure that takes a parameter (in this case, a variable) and uses it in a query:

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

You can then execute this stored procedure and provide a value for the `@EmployeeID` parameter.

```sql
EXEC GetEmployeeDetails @EmployeeID = 101;
```

These examples should give you a basic understanding of how to declare, assign values to, and use variables in Microsoft SQL Server. Keep in mind that variables have a scope, so they are only valid within the batch or stored procedure where they are declared.

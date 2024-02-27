`sp_executesql` is a system stored procedure in SQL Server that is used to execute a Transact-SQL statement or batch that can be reused multiple times with different parameter values. It is particularly useful for executing dynamic SQL statements.

Here's a basic syntax of `sp_executesql`:

```sql
sp_executesql [@stmt = ] statement  
    [  
      {, [@params = ] N'@parameter_name data_type [ OUT | OUTPUT ][,...n]' }  
    {, [@param1 = ] 'value1' [,...n] }  
    [;]  
```

- `@stmt`: This is the SQL statement or batch that you want to execute. It can be either a Unicode string (`nvarchar`) or a non-Unicode string (`varchar`).
  
- `@params`: This is an optional parameter that specifies the parameters used in the SQL statement. It should be in the form of a parameter declaration list. Each parameter declaration consists of the parameter name, data type, and optionally `OUT` or `OUTPUT` keyword if the parameter is an output parameter.

- `@param1`, `@param2`, ...: These are the parameter values that correspond to the parameters defined in `@params`. They are provided in the same order as they appear in the parameter declaration list.

Here's an example of how to use `sp_executesql`:

```sql
DECLARE @sql NVARCHAR(MAX);
DECLARE @param NVARCHAR(50) = 'John';

SET @sql = N'SELECT * FROM Employees WHERE FirstName = @firstName';

EXEC sp_executesql @sql, N'@firstName NVARCHAR(50)', @firstName = @param;
```

In this example, `@sql` contains the SQL statement to be executed, and `@param` is the parameter value. The `sp_executesql` stored procedure is then used to execute the SQL statement with the provided parameter value.

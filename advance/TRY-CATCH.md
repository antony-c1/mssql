# TRY...CATCH

[Documentation](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/try-catch-transact-sql?view=sql-server-ver16)

In SQL Server, the `TRY...CATCH` construct is used for error handling. It allows you to handle errors that occur during the execution of a Transact-SQL statement or batch.

Here is a simple example of how to use `TRY...CATCH`:

```sql
BEGIN TRY
    -- Code that might cause an error
    SELECT 1 / 0; -- Division by zero to trigger an error
END TRY
BEGIN CATCH
    -- Code to handle the error
    SELECT ERROR_MESSAGE() AS ErrorMessage;
END CATCH;
```

In this example, the code within the `TRY` block attempts to perform a division by zero, which would normally raise an error. When an error occurs, the control is transferred to the `CATCH` block, where you can handle the error.

The `ERROR_MESSAGE()` function is used to retrieve the error message associated with the last error that occurred. You can use other error functions like `ERROR_NUMBER()`, `ERROR_SEVERITY()`, etc., to get additional information about the error.

You can also nest `TRY...CATCH` blocks for more complex error handling scenarios. Always make sure to include appropriate error-handling logic to handle errors gracefully in your application.

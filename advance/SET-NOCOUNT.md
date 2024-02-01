# SET NOCOUNT

The `SET NOCOUNT` statement is used in Transact-SQL (T-SQL) to control the message returned to the client about the number of rows affected by a Transact-SQL statement. When `SET NOCOUNT` is turned ON, the message indicating the number of rows affected is not sent to the client.

Here's how it works:

- `SET NOCOUNT ON;`: When this statement is executed at the beginning of a stored procedure or a batch of T-SQL statements, it prevents the "x rows affected" message from being sent to the client after each statement. This can be useful to reduce network traffic, especially for stored procedures that perform multiple operations.

- `SET NOCOUNT OFF;`: This statement is used to revert to the default behavior, where the message indicating the number of rows affected is sent to the client.

Example:

```sql
CREATE PROCEDURE SampleProcedure
AS
BEGIN
    SET NOCOUNT ON;

    -- T-SQL statements go here

    SET NOCOUNT OFF;
END;
```

In the example above, `SET NOCOUNT ON;` is used to suppress the row count messages for the duration of the stored procedure, and `SET NOCOUNT OFF;` is used to revert to the default behavior afterward.

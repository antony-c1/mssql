# SET NOCOUNT

[Documentation](https://learn.microsoft.com/en-us/sql/t-sql/statements/set-nocount-transact-sql?view=sql-server-ver16)

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

## FAQ
<details>
    <summary>can procedure contain only this <b>`SET NOCOUNT ON</b>?</summary>

Yes, a stored procedure can indeed contain only the `SET NOCOUNT ON` statement. This is especially common when the stored procedure doesn't return any result sets and its primary purpose is to perform some operations without sending row count messages to the client.

Here's an example of a simple stored procedure with just the `SET NOCOUNT ON` statement:

```sql
CREATE PROCEDURE SampleProcedure
AS
BEGIN
    SET NOCOUNT ON;

    -- Your business logic or operations go here

END;
```

In this case, `SET NOCOUNT ON` is used to suppress the row count messages, and the body of the stored procedure can contain the necessary T-SQL statements or business logic without the additional overhead of sending row count messages to the client.
</details>

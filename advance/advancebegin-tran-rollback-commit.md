# BEGIN TRAN, ROLLBACK, COMMIT
In Microsoft SQL Server (MSSQL), `BEGIN TRAN`, `ROLLBACK`, and `COMMIT` are used to manage transactions. A transaction is a sequence of one or more SQL statements that are executed as a single unit of work. Transactions ensure the consistency and integrity of a database. Here's a brief explanation of each:

1. **BEGIN TRAN (Begin Transaction):**
   - `BEGIN TRAN` is used to mark the beginning of a transaction.
   - Once a transaction begins, a series of SQL statements can be executed, and the changes made by those statements are not visible to other transactions until the transaction is committed.
   - The transaction remains open until it is either committed or rolled back.

   Example:
   ```sql
   BEGIN TRAN;
   -- SQL statements within the transaction
   ```

2. **ROLLBACK:**
   - `ROLLBACK` is used to undo changes made during the current transaction.
   - If an error occurs or if the transaction needs to be canceled for any reason, `ROLLBACK` is used to revert the database to its state before the `BEGIN TRAN`.

   Example:
   ```sql
   ROLLBACK;
   ```

3. **COMMIT:**
   - `COMMIT` is used to finalize the changes made during the transaction and make those changes permanent.
   - Once `COMMIT` is issued, the changes are visible to other transactions, and the transaction is considered complete.

   Example:
   ```sql
   COMMIT;
   ```

**Usage Example:**
```sql
BEGIN TRAN;

BEGIN TRY
    -- SQL statements within the transaction
    UPDATE TableName SET Column1 = Value1 WHERE SomeCondition;

    -- If everything is successful, commit the transaction
    COMMIT;
END TRY
BEGIN CATCH
    -- If an error occurs, rollback the transaction
    ROLLBACK;
    PRINT ERROR_MESSAGE();
END CATCH;
```

In this example, the `BEGIN TRAN` marks the beginning of a transaction. The `COMMIT` is executed if all the SQL statements within the transaction run successfully. If an error occurs (caught by the `BEGIN CATCH` block), the `ROLLBACK` is executed to undo any changes made during the transaction.

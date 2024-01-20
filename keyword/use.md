# USE

In SQL Server, `USE` is a keyword used to specify the database context within which the subsequent SQL statements will be executed. It's not a function or a property but a command that changes the current database for the connection.

### Syntax:

```sql
USE database_name;
```

### Purpose of the `USE` Keyword:

1. **Database Switching:**
   - The primary purpose of the `USE` keyword is to switch the context to a different database. When you execute the `USE` statement, subsequent SQL statements will be executed in the specified database.

   ```sql
   USE YourDatabase;
   ```

2. **Querying or Modifying Specific Database:**
   - If you have multiple databases in your SQL Server instance, you can use the `USE` statement to specify the database you want to query or modify.

   ```sql
   USE SalesDatabase;
   SELECT * FROM SalesTable;
   ```

3. **Database Maintenance:**
   - It's commonly used in scripts and stored procedures where you need to ensure that the subsequent statements are executed in a specific database.

   ```sql
   USE ArchiveDatabase;
   DELETE FROM OldRecordsTable WHERE Date < '2020-01-01';
   ```

### Example:

```sql
-- Switch to the "YourDatabase" database
USE YourDatabase;

-- Execute a query in the specified database
SELECT * FROM YourTable;
```

### Important Considerations:

1. **Permissions:**
   - The user executing the `USE` statement must have the necessary permissions to access the specified database. If the user doesn't have permission, the `USE` statement will fail.

2. **Temporary Context Change:**
   - The effect of the `USE` statement is temporary and applies only to the current connection. It does not change the default database associated with the login.

3. **Connection Pooling:**
   - In applications using connection pooling, the database context might persist across different queries. It's essential to be aware of the database context in a pooled connection.

### Use Cases:

1. **Multi-Tenant Environments:**
   - When working with multiple databases in a multi-tenant environment, the `USE` statement helps switch between the databases for different clients.

2. **Stored Procedures and Scripts:**
   - It's commonly used at the beginning of stored procedures or scripts to set the context for the subsequent statements.

3. **Database Administration:**
   - When performing maintenance tasks or administrative operations, the `USE` statement helps ensure that the statements are executed in the correct database.

In summary, the `USE` keyword is a tool for managing the current database context in SQL Server, allowing you to execute queries or modifications in a specific database. It's a fundamental part of working with multiple databases within a SQL Server instance.

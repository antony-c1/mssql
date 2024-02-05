# sp_help

The `sp_help` stored procedure in SQL Server is a system procedure that provides information about a database object. Its purpose is to display detailed information about a table, view, or stored procedure, including columns, data types, identity information, constraints, and indexes.

Here's a basic usage example:

```sql
-- To get information about a table
EXEC sp_help 'YourTableName';
```

Replace 'YourTableName' with the name of the table for which you want to retrieve information.

This procedure can be useful when you need a quick overview of the structure and characteristics of a database object. It can help you understand the schema, primary and foreign keys, indexes, and other properties associated with the specified object.

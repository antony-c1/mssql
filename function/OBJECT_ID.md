# OBJECT_ID

`OBJECT_ID()` is a function in Microsoft SQL Server that returns the object identification number (ID) of a specified object. It takes the object name (as a string) as an argument and returns the ID if the object exists; otherwise, it returns NULL.

Here's the basic syntax:

```sql
OBJECT_ID ( '[ database_name . [ schema_name ] . | schema_name . ] object_name' [ ,'object_type' ] )
```

- `database_name`: Optional. The name of the database where the object resides.
- `schema_name`: Optional. The name of the schema where the object resides.
- `object_name`: The name of the object for which to obtain the ID.
- `object_type`: Optional. The type of the object (e.g., 'U' for a table, 'V' for a view, 'P' for a stored procedure).

Example:

```sql
-- Check if a table exists in the current database
IF OBJECT_ID('dbo.YourTableName', 'U') IS NOT NULL
    PRINT 'Table exists';
ELSE
    PRINT 'Table does not exist';
```

In this example, `OBJECT_ID()` is used to check if a table named 'YourTableName' exists in the 'dbo' schema. The second parameter ('U') indicates that we are checking for a table.

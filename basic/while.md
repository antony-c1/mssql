# WHILE
In MSSQL, the `WHILE` loop is used to repeatedly execute a block of SQL statements as long as the specified condition is true. The general syntax of the `WHILE` loop is as follows:

```sql
WHILE condition
BEGIN
    -- SQL statements to be executed repeatedly

    -- Update condition (to avoid an infinite loop)
    -- (e.g., increment a counter or modify a variable)
END
```

Here's a simple example that uses a `WHILE` loop to print numbers from 1 to 5:

```sql
DECLARE @Counter INT = 1;

WHILE @Counter <= 5
BEGIN
    PRINT 'Counter: ' + CAST(@Counter AS NVARCHAR(10));
    
    -- Update the counter
    SET @Counter = @Counter + 1;
END
```

In this example:

- `DECLARE @Counter INT = 1;`: Initializes a variable `@Counter` with an initial value of 1.

- `WHILE @Counter <= 5`: Specifies the condition that needs to be true for the loop to continue.

- `BEGIN...END`: Defines the block of SQL statements to be executed repeatedly as long as the condition is true.

- `PRINT 'Counter: ' + CAST(@Counter AS NVARCHAR(10));`: Prints the current value of the counter.

- `SET @Counter = @Counter + 1;`: Updates the counter to increment its value.

The loop will continue executing until the condition `@Counter <= 5` becomes false. Note that it's important to have a mechanism (like updating the counter) to eventually make the condition false; otherwise, the loop could run indefinitely, resulting in an infinite loop.

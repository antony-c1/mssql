# N prefix
In SQL Server, the `N` prefix before a string literal indicates that the string should be treated as Unicode. Unicode is a character encoding standard that supports a broader range of characters, including characters from many languages and special symbols.

When you use parameters in SQL queries, it's a good practice to specify Unicode strings (when necessary) by prefixing the string literal with `N`. This ensures that the query handles Unicode characters correctly, especially when dealing with non-English text or special characters.

In the syntax you provided:

```sql
N'SELECT * FROM Employees WHERE FirstName = @firstName';
```

The `N` prefix is used before the string `'SELECT * FROM Employees WHERE FirstName = @firstName'`, indicating that it's a Unicode string. This is particularly important when the string contains non-ASCII characters, as it ensures proper handling and storage of those characters in SQL Server.

# REPLACE

In Microsoft SQL Server, the `REPLACE` function is used to replace all occurrences of a specified string value with another string value within a string. Here's the syntax:

```sql
REPLACE(string_expression, string_pattern, string_replacement)
```

- `string_expression`: The original string where replacements will occur.
- `string_pattern`: The substring to be replaced.
- `string_replacement`: The string to replace occurrences of `string_pattern`.

For example:

```sql
SELECT REPLACE('Hello, World!', 'World', 'Universe') AS Result;
```

This query will return `'Hello, Universe!'` because it replaced the substring `'World'` with `'Universe'` in the original string `'Hello, World!'`.

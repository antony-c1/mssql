# Store Procedure

In Microsoft SQL Server, a stored procedure is a precompiled collection of one or more Transact-SQL statements or batches that are stored as a single object in the database. Stored procedures can be called to perform a specific task or a set of tasks. Here is a basic syntax for creating a stored procedure:

```sql
CREATE PROCEDURE ProcedureName
    @Parameter1 DataType1,
    @Parameter2 DataType2
AS
BEGIN
    -- SQL statements to implement the procedure logic
END;
```

Here's a more detailed explanation:

- `ProcedureName`: The name of the stored procedure.
- `@Parameter1`, `@Parameter2`: Input parameters for the stored procedure, each with its data type.
- `AS`: The keyword that begins the body of the stored procedure.
- `BEGIN` and `END`: Delimiters that enclose the body of the stored procedure.
- The body of the stored procedure consists of one or more Transact-SQL statements that implement the logic of the procedure.

Here's an example of a simple stored procedure that retrieves employee details based on an employee ID:

```sql
CREATE PROCEDURE GetEmployeeDetails
    @EmployeeID INT
AS
BEGIN
    SELECT *
    FROM Employees
    WHERE EmployeeID = @EmployeeID;
END;
```

You can execute the stored procedure like this:

```sql
EXEC GetEmployeeDetails @EmployeeID = 101;
```

Stored procedures can also have output parameters, return values, and can execute other stored procedures or SQL statements. They provide a way to encapsulate and reuse logic within the database. Additionally, stored procedures can enhance performance by reducing the need to send multiple queries over the network.

Remember to adapt the stored procedure based on your specific requirements and the structure of your database.

## Nmaing Store Procedure
Simply Use `sp` (stored Procedure) or `usp` (User Stored Procedure) for the **Prefix** or `csp` (Custom Stored Procedure) to increase the readability and maintainability.
<details>
    <summary>More Info</summary>


    Naming conventions for stored procedures, like any other code elements, help improve readability, maintainability, and consistency across your database. While specific conventions can vary between organizations and developers, here are some common practices for naming stored procedures in Microsoft SQL Server:

1. **Prefix:**
   - Consider using a consistent prefix to distinguish stored procedures from other database objects. Common prefixes include `usp_` (user stored procedure) or `sproc_`.

   ```sql
   CREATE PROCEDURE usp_GetEmployeeDetails
   ```

2. **Verb-Noun Format:**
   - Use a clear and descriptive verb-noun format to indicate the action performed by the stored procedure.

   ```sql
   CREATE PROCEDURE usp_GetEmployeeDetails
   ```

3. **Avoid Ambiguous Abbreviations:**
   - Avoid ambiguous or unclear abbreviations. Choose abbreviations that are widely understood or use full words for better readability.

   ```sql
   CREATE PROCEDURE usp_GetCustomerOrders
   ```

4. **Consistent Casing:**
   - Use consistent casing for stored procedure names. Common choices include PascalCase or snake_case.

   ```sql
   CREATE PROCEDURE usp_GetCustomerDetails
   ```

5. **Avoid Special Characters:**
   - Avoid using special characters or spaces in stored procedure names. Stick to alphanumeric characters and underscores.

   ```sql
   CREATE PROCEDURE usp_GetProductPrices
   ```

6. **Use Singular Nouns:**
   - Use singular nouns for stored procedure names to maintain consistency and align with standard naming practices.

   ```sql
   CREATE PROCEDURE usp_GetProductDetails
   ```

7. **Include Entity Name:**
   - Include the name of the entity the stored procedure operates on to provide context.

   ```sql
   CREATE PROCEDURE usp_GetCustomerOrders
   ```

8. **Versioning (if necessary):**
   - If you need to version your stored procedures, consider including a version number in the name.

   ```sql
   CREATE PROCEDURE usp_GetCustomerOrders_v2
   ```

9. **Camel Case for Parameters:**
   - If your stored procedure has parameters, consider using camelCase for their names.

   ```sql
   CREATE PROCEDURE usp_GetEmployeeDetails
       @employeeId INT
   ```

10. **Avoid Reserved Words:**
   - Avoid using SQL Server reserved words as stored procedure names.

   ```sql
   CREATE PROCEDURE usp_RetrieveAllCustomers
   ```

By adhering to a consistent naming convention, you make it easier for developers to understand the purpose of each stored procedure and maintain a clean and organized database schema. Remember to document your stored procedures to provide additional context and usage information.
</details>

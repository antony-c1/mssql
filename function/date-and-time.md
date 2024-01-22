# DATE AND TIME

Microsoft SQL Server (MSSQL) provides various date and time functions to work with date and time values. Here are some commonly used date and time functions in MSSQL:

1. **GETDATE():**
   - Returns the current date and time from the system.

   ```sql
   SELECT GETDATE() AS CurrentDateTime;
   ```

2. **SYSDATETIME():**
   - Returns a `datetime2` value that contains the date and time of the computer on which the instance of SQL Server is running.

   ```sql
   SELECT SYSDATETIME() AS CurrentDateTime;
   ```

3. **CURRENT_TIMESTAMP:**
   - Returns the current date and time as a `datetime` value.

   ```sql
   SELECT CURRENT_TIMESTAMP AS CurrentDateTime;
   ```

4. **FORMAT():**
   - Formats a date and time value.

   ```sql
   SELECT FORMAT(GETDATE(), 'MM/dd/yyyy HH:mm:ss') AS FormattedDateTime;
   ```

5. **DATEDIFF():**
   - Returns the difference between two dates.

   ```sql
   SELECT DATEDIFF(DAY, '2022-01-01', '2022-01-10') AS DateDifference;
   ```

6. **DATEADD():**
   - Adds or subtracts a specified time interval from a date.

   ```sql
   SELECT DATEADD(DAY, 7, '2022-01-01') AS NewDate;
   ```

7. **DATEPART():**
   - Returns a specified part of a date.

   ```sql
   SELECT DATEPART(YEAR, '2022-01-01') AS Year;
   ```

8. **MONTH():**
   - Returns the month part of a date.

   ```sql
   SELECT MONTH('2022-01-01') AS Month;
   ```

9. **YEAR():**
   - Returns the year part of a date.

   ```sql
   SELECT YEAR('2022-01-01') AS Year;
   ```

10. **CONVERT():**
    - Converts a date and time from one data type to another.

    ```sql
    SELECT CONVERT(VARCHAR, GETDATE(), 120) AS FormattedDateTime;
    ```

11. **DATEDIFF_BIG():**
    - Similar to `DATEDIFF()`, but supports a larger date range.

    ```sql
    SELECT DATEDIFF_BIG(SECOND, '2022-01-01', '2022-01-10') AS DateDifferenceInSeconds;
    ```

These functions provide flexibility for working with date and time values in MSSQL, allowing you to perform various calculations and manipulations.

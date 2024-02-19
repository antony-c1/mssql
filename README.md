# MSSQL
`Microsoft SQL` Server is a proprietary `relational database` management system developed by **Microsoft**. As a database server, it is a software product with the primary function of storing and retrieving data.

![image](https://github.com/Antony-M1/mssql/assets/96291963/ddf095cd-1e1c-4fbd-a22e-1177d02953d2)

## Reference Tutorials
1. [SQL Server - How to use SQL Profiler - FoxLearn](https://www.youtube.com/watch?v=mkGoK8X0X3o)

# Table Of Content
### Keyword
1. [USE](./keyword/use.md)


### Property
1. [IDENTITY](./property/identity.md)
2. [Variables](./property/variables.md)


### Basic
1. [BEGIN & END](./basic/begin-end.md)
2. [WHILE](basic/while.md)
3. [TOP, LIMIT, FETCH FIRST, ROWNUM](basic/TOP-LIMIT-FETCH_FIRST-ROWNUM.md)
4. [NULL LAST](basic/null-last.md)


### Advance
1. [Store Procedure](./advance/store_procedure.md)
2. [BEGIN TRAN, ROLLBACK, COMMIT](./advance/advancebegin-tran-rollback-commit.md)
3. [Function](advance/function.md)
4. [SET NOCOUNT](advance/SET-NOCOUNT.md)
5. [TRY..CATCH](advance/TRY-CATCH.md)
### Function
1. [OBJECT_ID](/function/OBJECT_ID.md)
2. [DATE & TIME](function/date-and-time.md)
3. [ISNULL](function/isnull.md)

### System Procedure
1. [sp_depends](procedure/sp_depends.md)
2. [sp_columns](procedure/sp_columns.md)
3. [sp_help](procedure/sp_help.md)
4. [sp_helpconstraint](procedure/sp_helpconstraint.md)
5. [sp_helpindex](procedure/sp_helpindex.md)
6. [sp_tables](procedure/sp_tables.md)
7. [sp_stored_procedures](procedure/sp_stored_procedures.md)
# Debugger
* [How to debug SQL code](https://www.youtube.com/watch?v=wng_eetygXM)
* [Stored Procedure debugging in sql - sql debugging stored procedures](https://www.youtube.com/watch?v=BDswTNxnFAA)
* [How to: Debug Database Objects](https://learn.microsoft.com/en-us/sql/ssdt/how-to-debug-database-objects?view=sql-server-ver16)

# Backup
In Microsoft SQL Server, the backup file extension is typically `.bak`. When you perform a backup operation on a SQL Server database, it creates a backup file with the `.bak` extension by default. This file contains a copy of the database at the time the backup was taken, allowing you to restore the database to that point in time if needed.

For example, if you perform a backup of a database named `MyDatabase`, the resulting backup file might be named something like `MyDatabase.bak`.

You can create backups using SQL Server Management Studio (SSMS) or by running T-SQL commands such as `BACKUP DATABASE` or `BACKUP LOG`.

**YouTupe**
* [How To Backup A Database in Microsoft SQL Server (MSSQL) Management Studio [English 2020]](https://www.youtube.com/watch?v=S6uo4_f0Gvw)

### Schedule Backup
* [Scheduled Automatic SQL Database Backup using SSMS](https://www.youtube.com/watch?v=D0zuWkBdedI)

# Restore
In Microsoft SQL Server (MSSQL), "restore" refers to the process of recovering a database from a backup file. It involves taking a previously created backup of a database and restoring it to its original state or to a new location. This is a critical operation in database management, often used to recover from data loss, corruption, or other disasters.

During a restore operation, the backup file (typically with a `.bak` extension) is read and its contents are used to recreate the database, including its tables, indexes, stored procedures, and other objects. The restore process can overwrite an existing database or create a new one, depending on the options chosen.

There are different types of restore operations in MSSQL, including:
- **Full Restore**: Recovers the entire database from a full backup.
- **Differential Restore**: Restores only the data that has changed since the last full backup.
- **Transaction Log Restore**: Recovers the database to a specific point in time by applying transaction log backups.
- **Filegroup Restore**: Recovers only specific filegroups within a database.

Overall, the restore operation is essential for maintaining data integrity and ensuring that databases can be recovered in case of unexpected failures or errors.

**YouTube**
* [SQL Server 2019 - SSMS 2018 - Backup and Restore Databases From One Server To Another server](https://www.youtube.com/watch?v=B9-bpeNZnVs)

# SSRS Report

**SSRS** stands for `SQL Server Reporting Services`. It is a `server-based` report generation software system from `Microsoft`. It provides a set of tools and services that enable the creation, management, and delivery of interactive and `printed reports`. `SSRS` allows users to design reports using various data sources, including relational databases like `Microsoft SQL Server`, `Oracle`, `MySQL`, and others.

**Note:** `SSRS` is old technology for `generating` and `publishing` reports based on the programming and coding interface. In contrast, `Power BI` is more friendly, advanced, easy to use, and has more graphical and visualization tools.

**YouTube:**
* [Learn how to create SQL Reports SSRS in less than 5 minutes, ssrs tutorial for beginners](https://www.youtube.com/watch?v=Zfc6jExS4Gk)

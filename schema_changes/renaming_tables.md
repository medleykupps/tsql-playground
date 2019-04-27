# Renaming database tables

Use the stored procedure `sp_rename`. 

Official Microsoft Docs: https://docs.microsoft.com/en-us/sql/relational-databases/system-stored-procedures/sp-rename-transact-sql?view=sql-server-2017.

This will rename a table `Transactions` to `Transactions_Backup`.
```
EXEC sp_rename 'Transactions', 'Transactions_Backup'
```

And, this renames to back
```
EXEC sp_rename 'Transactions_Backup', 'Transactions'
```

Also, can be used for:

- index
- column
- alias data type
- CLR user-defined type


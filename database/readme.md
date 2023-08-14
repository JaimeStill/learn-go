# Go Notes

Add the `mysql` CLI to PATH for execution in PowerShell

```powershell
$env:Path += ';C:\Program Files\MySql\MySql Server 8.0\bin'
```

Add `DBUSER` and `DBPASS` environment variables:

```powershell
$env:DBUSER='root'
$env:DBPASS='password'
```

Connect to MySQL:

```powershell
mysql -u root -p
Enter password: *******
mysql>
```

Create a database and initialize a table:

```sql
create database recordings;
use recordings;
source create-tables.sql

select * from album;
```

```
+----+---------------+----------------+-------+
| id | title         | artist         | price |
+----+---------------+----------------+-------+
|  1 | Blue Train    | John Coltrane  | 56.99 |
|  2 | Giant Steps   | John Coltrane  | 63.99 |
|  3 | Jeru          | Gerry Mulligan | 17.99 |
|  4 | Sarah Vaughan | Sarah Vaughan  | 34.98 |
+----+---------------+----------------+-------+
4 rows in set (0.00 sec)
```
# EF Migration

## Create the migration of database

[Follow these steps for generating of DB migrations](/README.md#ef-core--data-access)

## Using other database engines

### PostgreSQL

Install following NuGet package:

```text
Npgsql.EntityFrameworkCore.PostgreSQL
Npgsql.EntityFrameworkCore.PostgreSQL.Design
```

In `Helpers\StartupHelpers.cs` - find all usage of `UseSqlServer` and change to `UseNpgsql`.

> **_NOTE:_** Don't forget to update your connection string in `appsettings.json` and (re)generate migrations for new database

### SQLite

Install following NuGet package:

```text
Microsoft.EntityFrameworkCore.Sqlite
Microsoft.EntityFrameworkCore.Sqlite.Design
```

In `Helpers\StartupHelpers.cs` - find all usage of `UseSqlServer` and change to `UseSqlite`.

> **_NOTE:_** Don't forget to update your connection string in `appsettings.json` and (re)generate migrations for new database

### MySQL and MariaDB

Install the following NuGet package:

```text
Pomelo.EntityFrameworkCore.MySql
Pomelo.EntityFrameworkCore.MySql.Design
```

In `Helpers\StartupHelpers.cs` - find all usage of `UseSqlServer` and change to `UseMySql`.

> **_NOTE:_** Don't forget to update your connection string in `appsettings.json` and (re)generate migrations for new database

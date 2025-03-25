# fourzer.EntityFrameworkCore.Naming

`fourzer.EntityFrameworkCore.Naming` is a lightweight .NET library that provides an extension method to automatically convert table names, column names, keys, constraints, and indexes to `snake_case` in Entity Framework Core.

This is especially useful when working with databases like PostgreSQL or MySQL, which conventionally use `snake_case` naming for identifiers.

---

## ✨ Features

- Applies `snake_case` naming to:
  - Table names
  - Column names
  - Primary and foreign keys
  - Indexes and constraints
- Plug-and-play with any EF Core model
- Compatible with all relational EF Core providers (PostgreSQL, MySQL, SQL Server, Oracle, etc.)
- .NET 6 and .NET Standard 2.1 support

---

## 📌 Requirements
- .NET 6.0 or .NET Standard 2.1+
- Entity Framework Core 6.0+

---

## 📦 Installation

You can install via [NuGet.org](https://www.nuget.org/packages/fourzer.EntityFrameworkCore.Naming):

```bash
dotnet add package fourzer.EntityFrameworkCore.Naming
```
## 🚀 Usage

In your DbContext, apply the extension method in OnModelCreating:
```bash
using Microsoft.EntityFrameworkCore;
using fourzer.EntityFrameworkCore.Naming;

public class AppDbContext : DbContext
{
    protected override void OnModelCreating(ModelBuilder modelBuilder)
    {
        modelBuilder.UseSnakeCase(); // Converts everything to snake_case
    }
}

```

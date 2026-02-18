# AlpinPastaParti – Database + ASP.NET Web Interface
**CSE3055 – Database Systems (Project Step #4)**

This project implements a **Microsoft SQL Server** database for a party organization business (Alpin Pasta Parti) and provides a simple **ASP.NET WebForms (.NET Framework, C#)** interface to interact with the database.

## What’s Inside

### Database (MS SQL Server)
Core SQL scripts included:
- `CreationTables.sql` — creates (and recreates) the `AlpinPastaParti` database and tables
- `Insertion.sql` — inserts sample data
- `Views.sql` — database views for reporting/querying
- `StoredProcedure.sql` — stored procedures used by the web interface (e.g., customer CRUD operations)
- `TRIGGER.sql` — trigger example(s)

### Web Interface (ASP.NET WebForms)
- Solution: `AlpinPastaParti.sln`
- Project: `AlpinPastaParti.csproj`
- Example page: `Customer.aspx`  
  Provides basic operations such as:
  - Insert new customer
  - Delete customer
  - View customer information  
  (via stored procedures on SQL Server)

## Requirements
- **Microsoft SQL Server** (LocalDB / Express / Developer / Standard)
- **Visual Studio** (recommended: 2019/2022) with **.NET Framework** support
- NuGet packages (restored via `packages.config`)

## Setup (Database)

> ⚠️ `CreationTables.sql` drops and recreates the database `AlpinPastaParti`.
> Run it only if you are OK with recreating the DB.

1) Open SQL Server Management Studio (SSMS)  
2) Run scripts in this order:

1. `CreationTables.sql`
2. `Insertion.sql` (optional but recommended for sample data)
3. `Views.sql`
4. `StoredProcedure.sql`
5. `TRIGGER.sql` (optional, for trigger demonstration)

## Setup (Web Application)

1) Open `AlpinPastaParti.sln` in Visual Studio  
2) Restore packages:
   - Right click Solution → **Restore NuGet Packages** (or build once)
3) Check the DB connection string in:
   - `Web.config`

Make sure it points to your SQL Server instance and the `AlpinPastaParti` database.

4) Run the project:
   - Press **F5** (IIS Express)

## Notes
- Stored procedures are used to keep DB operations consistent and reusable.
- The project report is included as: `Project Report.docx`.

## Author
- Rana

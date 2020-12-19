#### Task 3: Get SQL database records by using Entity Framework

1.  Within the **Main** method, add the following blocks of code to export all model and product records from SQL Database to local memory:

    ```
    await Console.Out.WriteLineAsync("Start Migration");

    using AdventureWorksSqlContext context = new AdventureWorksSqlContext(sqlDBConnectionString);

    List<Model> items = await context.Models
        .Include(m => m.Products)
        .ToListAsync<Model>();

    await Console.Out.WriteLineAsync($"Total Azure SQL DB Records: {items.Count}");
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, change your context to the **AdventureWorks.Migrate** folder:

    ```
    cd .\AdventureWorks.Migrate\
    ```

1.  Using the same terminal, build the .NET console application project:

    ```
    dotnet build
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\04\\Solution\\AdventureWorks\\AdventureWorks.Migrate** folder.

1.  Close the current terminal.
#### Task 1: Create a migration project

1.  Using a terminal, create a new .NET console project named **AdventureWorks.Migrate** in a folder with the same name:

    ```
    dotnet new console --name AdventureWorks.Migrate
    ```

    > **Note**: The **dotnet new** command will create a new **console** project in a folder with the same name as the project.

1.  Using the same terminal, add a reference to the existing **AdventureWorks.Models** project:

    ```
    dotnet add .\AdventureWorks.Migrate\AdventureWorks.Migrate.csproj reference .\AdventureWorks.Models\AdventureWorks.Models.csproj
    ```

    > **Note**: The **dotnet add reference** command will add a reference to the model classes contained in the **AdventureWorks.Models** project.

1.  Using the same terminal, add a reference to the existing **AdventureWorks.Context** project:

    ```
    dotnet add .\AdventureWorks.Migrate\AdventureWorks.Migrate.csproj reference .\AdventureWorks.Context\AdventureWorks.Context.csproj
    ```

    > **Note**: The **dotnet add reference** command will add a reference to the context classes contained in the **AdventureWorks.Context** project.

1.  Using the same terminal, change your context to the **AdventureWorks.Migrate** folder:

    ```
    cd .\AdventureWorks.Migrate\
    ```

1.  Using the same terminal, import version 3.0.1 of **Microsoft.EntityFrameworkCore.SqlServer** from NuGet:

    ```
    dotnet add package Microsoft.EntityFrameworkCore.SqlServer --version 3.0.1
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.EntityFrameworkCore.SqlServer** package from **NuGet**. For more information, go to: [Microsoft.EntityFrameworkCore.SqlServer](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/3.0.1).

1.  Using the same terminal, import version 3.4.1 of **Microsoft.Azure.Cosmos** from NuGet:

    ```
    dotnet add package Microsoft.Azure.Cosmos --version 3.4.1
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.Azure.Cosmos** package from **NuGet**. For more information, go to: [Microsoft.Azure.Cosmos](https://www.nuget.org/packages/Microsoft.Azure.Cosmos/3.4.1).

1.  Using the same terminal, build the .NET console application:

    ```
    dotnet build
    ```

1.  Close the current terminal.
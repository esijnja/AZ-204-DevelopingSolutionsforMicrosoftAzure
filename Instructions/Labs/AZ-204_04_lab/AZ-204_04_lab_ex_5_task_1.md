#### Task 1: Update library with the Cosmos SDK and references

1.  Using a terminal, change your context to the **AdventureWorks.Context** folder:

    ```
    cd .\AdventureWorks.Context\
    ```

1.  Using the same terminal, import **Microsoft.Azure.Cosmos** from NuGet:

    ```
    dotnet add package Microsoft.Azure.Cosmos --version 3.4.1
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.Azure.Cosmos** package from **NuGet**. For more information, go to: [Microsoft.Azure.Cosmos](https://www.nuget.org/packages/Microsoft.Azure.Cosmos/3.4.1).

1.  Using the same terminal, build the ASP.NET web application project:

    ```
    dotnet build
    ```

1.  Close the current terminal.
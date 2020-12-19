#### Task 1: Import the Microsoft Graph SDK from NuGet

1.  Using a terminal, import version 1.21.0 of **Microsoft.Graph** from NuGet:

    ```
    dotnet add package Microsoft.Graph --version 1.21.0
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.Graph** package from NuGet. For more information, go to [Microsoft.Graph](https://www.nuget.org/packages/Microsoft.Graph/1.21.0).

1.  Using the same terminal, import version 1.0.0-preview.2 of **Microsoft.Graph.Auth** from NuGet:

    ```
    dotnet add package Microsoft.Graph.Auth --version 1.0.0-preview.2
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.Graph.Auth** package from NuGet. For more information, go to [Microsoft.Graph.Auth](https://www.nuget.org/packages/Microsoft.Graph.Auth/1.0.0-preview.2).

1.  Using the same terminal, build the .NET web application:

    ```
    dotnet build
    ```

1.  Close the current terminal.
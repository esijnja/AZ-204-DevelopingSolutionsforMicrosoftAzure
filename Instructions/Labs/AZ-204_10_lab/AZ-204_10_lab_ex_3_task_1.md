#### Task 1: Create .NET project

1.  Using Visual Studio Code, open the **Allfiles (F):\\Allfiles\\Labs\\10\\Starter\\EventPublisher** folder.

1.  Using a terminal, create a new .NET project named **EventPublisher** in the current folder:

    ```
    dotnet new console --name EventPublisher --output .
    ```

    > **Note**: The **dotnet new** command will create a new **console** project in a folder with the same name as the project.

1.  Using the same terminal, import version 3.2.0 of **Microsoft.Azure.EventGrid** from NuGet:

    ```
    dotnet add package Microsoft.Azure.EventGrid --version 3.2.0
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.Azure.EventGrid** package from NuGet. For more information, go to [Microsoft.Azure.EventGrid](https://www.nuget.org/packages/Microsoft.Azure.EventGrid/3.2.0).

1.  Using the same terminal, build the .NET web application:

    ```
    dotnet build
    ```

1.  Close the current terminal.
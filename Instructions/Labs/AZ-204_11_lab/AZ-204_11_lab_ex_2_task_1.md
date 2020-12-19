#### Task 1: Create a .NET project

1.  Using Visual Studio Code, open the **Allfiles (F):\\Allfiles\\Labs\\11\\Starter\\MessageProcessor** folder.

1.  Using a terminal, create a new .NET project named **MessageProcessor** in the current folder:

    ```
    dotnet new console --name MessageProcessor --output .
    ```

    > **Note**: The **dotnet new** command will create a new **console** project in a folder with the same name as the project.

1.  Using the same terminal, import version 12.0.0 of **Azure.Storage.Queues** from NuGet:

    ```
    dotnet add package Azure.Storage.Queues --version 12.0.0
    ```

    > **Note**: The **dotnet add package** command will add the **Azure.Storage.Queues** package from NuGet. For more information, go to [Azure.Storage.Queues](https://www.nuget.org/packages/Azure.Storage.Queues/12.0.0).

1.  Using the same terminal, build the .NET web application:

    ```
    dotnet build
    ```

1.  Close the current terminal.
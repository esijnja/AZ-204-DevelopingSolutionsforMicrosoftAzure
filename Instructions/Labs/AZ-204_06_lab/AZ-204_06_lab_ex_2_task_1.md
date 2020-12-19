#### Task 1: Create a .NET project

1.  Using Visual Studio Code, open the **Allfiles (F):\\Allfiles\\Labs\\06\\Starter\\GraphClient** folder.

1.  Using a terminal, create a new .NET project named **GraphClient** in the current folder:

    ```
    dotnet new console --name GraphClient --output .
    ```

    > **Note**: The **dotnet new** command will create a new **console** project in a folder with the same name as the project.

1.  Using the same terminal, import version 4.7.1 of **Microsoft.Identity.Client** from NuGet:

    ```
    dotnet add package Microsoft.Identity.Client --version 4.7.1
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.Identity.Client** package from NuGet. For more information, go to [Microsoft.Identity.Client](https://www.nuget.org/packages/Microsoft.Identity.Client/4.7.1).

1.  Using the same terminal, build the .NET web application:

    ```
    dotnet build
    ```

1.  Close the current terminal.
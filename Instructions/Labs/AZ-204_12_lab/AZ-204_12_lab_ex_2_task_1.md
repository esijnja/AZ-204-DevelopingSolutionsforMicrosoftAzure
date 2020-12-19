#### Task 1: Build a .NET Web API project

1.  Open Visual Studio Code.

1.  In Visual Studio Code, open the **Allfiles (F):\\Allfiles\\Labs\\12\\Starter\\Api** folder.

1.  Use the Explorer pane in Visual Studio Code to open a new terminal that has the context set to the current working directory.

1.  At the command prompt, create a new .NET Web API application named **SimpleApi** in the current directory:

    ```
    dotnet new webapi --output . --name SimpleApi
    ```

1.  Import version 2.14.0 of **Microsoft.ApplicationInsights** from NuGet to the current project:

    ```
    dotnet add package Microsoft.ApplicationInsights --version 2.14.0
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.ApplicationInsights** package from NuGet. For more information, go to [Microsoft.ApplicationInsights](https://www.nuget.org/packages/Microsoft.ApplicationInsights/2.14.0).

1.  Import version 2.14.0 of **Microsoft.ApplicationInsights.AspNetCore** from NuGet to the current project:

    ```
    dotnet add package Microsoft.ApplicationInsights.AspNetCore --version 2.14.0
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.ApplicationInsights.AspNetCore** package from NuGet. For more information, go to [Microsoft.ApplicationInsights.AspNetCore](https://www.nuget.org/packages/Microsoft.ApplicationInsights.AspNetCore/2.14.0).

1.  Import version 2.14.0 of **Microsoft.ApplicationInsights.PerfCounterCollector** from NuGet to the current project:

    ```
    dotnet add package Microsoft.ApplicationInsights.PerfCounterCollector  --version 2.14.0
    ```

    > **Note**: The **dotnet add package** command will add the **Microsoft.ApplicationInsights.PerfCounterCollector** package from NuGet. For more information, go to [Microsoft.ApplicationInsights.PerfCounterCollector](https://www.nuget.org/packages/Microsoft.ApplicationInsights.PerfCounterCollector/2.14.0).

1.  Build the .NET web app:

    ```
    dotnet build
    ```

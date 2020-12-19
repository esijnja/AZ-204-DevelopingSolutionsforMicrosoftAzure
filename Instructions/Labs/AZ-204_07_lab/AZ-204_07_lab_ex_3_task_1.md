#### Task 1: Initialize a function project

1. Open the **Windows Terminal** application.
1. Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\07\\Starter\\func** empty directory:

    ```powershell
    cd F:\Allfiles\Labs\07\Starter\func
    ```

1. Use the **Azure Functions Core Tools** to create a new local Azure Functions project with the following details:
    - worker runtime: **dotnet**

    ```powershell
    func init --worker-runtime dotnet
    ```

    > **Note**: You can review the documentation to [create a new project][azure-functions-core-tools-new-project] using the **Azure Functions Core Tools**.
1. **Build** the .NET Core 3.1 project:

    ```powershell
    dotnet build
    ```

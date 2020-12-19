#### Task 2: Pull and configure the Azure SDK for .NET

1. Open the **Windows Terminal** application.
1. Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\07\\Starter\\func** project directory.
1. When you receive the open command prompt, add version **12.6.0** of the **Azure.Storage.Blobs** package from NuGet:

    ```powershell
    dotnet add package Azure.Storage.Blobs --version 12.6.0
    ```

    > **Note**: The [Azure.Storage.Blobs](https://www.nuget.org/packages/Azure.Storage.Blobs/12.6.0) NuGet package references the subset of the Azure SDK for .NET required to write code for Azure Blob Storage.
1. Close the currently running **Windows Terminal** application.
1. Using **Visual Studio Code**, open the solution folder found at **Allfiles (F):\\Allfiles\\Labs\\07\\Starter\\func**.
1. Open the **FileParser.cs** file.
1. Add a **using directive** for the **Azure.Storage.Blobs** namespace:

    ```csharp
    using Azure.Storage.Blobs;
    ```

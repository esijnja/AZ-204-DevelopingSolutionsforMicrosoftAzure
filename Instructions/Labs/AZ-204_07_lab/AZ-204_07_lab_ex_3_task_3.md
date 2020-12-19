#### Task 3: Configure and read an application setting

1. Open **Visual Studio Code**.
1. Using **Visual Studio Code**, open the solution folder found at **Allfiles (F):\\Allfiles\\Labs\\07\\Starter\\func**.
1. Open the **local.settings.json** file.
1. Update the value of the **Values** object by adding a new setting named **StorageConnectionString** and setting it to a string value of **[TEST VALUE]**:

    ```json
    "Values": {
        "AzureWebJobsStorage": "UseDevelopmentStorage=true",
        "FUNCTIONS_WORKER_RUNTIME": "dotnet",
        "StorageConnectionString": "[TEST VALUE]"
    }
    ```

1. Open the **FileParser.cs** file.
1. In the code editor, delete all the code within the **FileParser.cs** file.
1. Add **using directives** for the **Microsoft.AspNetCore.Mvc**, **Microsoft.Azure.WebJobs**, **Microsoft.AspNetCore.Http**, **System**, and **System.Threading.Tasks** namespaces:

    ```csharp
    using Microsoft.AspNetCore.Mvc;
    using Microsoft.Azure.WebJobs;
    using Microsoft.AspNetCore.Http;
    using System;
    using System.Threading.Tasks;
    ```

1. Create a new **public static** class named **FileParser**:

    ```csharp
    public static class FileParser
    { }
    ```

1. Within the **FileParser** class, create a new **public static** *asynchronous* method named **Run** that returns a variable of type **Task\<IActionResult\>** and that also takes in a variable of type **HttpRequest** named *request*:

    ```csharp
    public static async Task<IActionResult> Run(
        HttpRequest request)
    { }
    ```

1. Append an attribute to the **Run** method of type **FunctionNameAttribute** that has its **name** parameter set to a value of **FileParser**:

    ```csharp
    [FunctionName("FileParser")]
    public static async Task<IActionResult> Run(
        HttpRequest request)
    { }
    ```

1. Append an attribute to the **request** parameter of type **HttpTriggerAttribute** that has its **methods** parameter array set to a single value of **GET**:

    ```csharp
    [FunctionName("FileParser")]
    public static async Task<IActionResult> Run(
        [HttpTrigger("GET")] HttpRequest request)
    { }
    ```

1. Within the **Run** method, retrieve the value of the **StorageConnectionString** application setting by using the **Environment.GetEnvironmentVariable** method and storing the result in a **string** variable named **connectionString**:

    ```csharp
    string connectionString = Environment.GetEnvironmentVariable("StorageConnectionString");
    ```

1. Finally, return the value of the **connectionString** variable as the HTTP response:

    ```csharp
    return new OkObjectResult(connectionString);
    ```

1. **Save** the **Echo.cs** file.
#### Task 2: Write HTTP-triggered function code

1. Open **Visual Studio Code**.
1. Using **Visual Studio Code**, open the solution folder found at **Allfiles (F):\\Allfiles\\Labs\\02\\Starter\\func**.
1. Open the **Echo.cs** file.
1. In the code editor, delete all the code within the **Echo.cs** file.
1. Add **using directives** for the **Microsoft.AspNetCore.Mvc**, **Microsoft.Azure.WebJobs**, **Microsoft.AspNetCore.Http**, and **Microsoft.Extensions.Logging** namespaces for libraries that will be referenced by the application:

    ```csharp
    using Microsoft.AspNetCore.Mvc;
    using Microsoft.Azure.WebJobs;
    using Microsoft.AspNetCore.Http;
    using Microsoft.Extensions.Logging;
    ```

1. Create a new **public static** class named **Echo**:

    ```csharp
    public static class Echo
    { }
    ```

1. Within the **Echo** class, create a new **public static** method named **Run** that returns a variable of type **IActionResult** and that also takes in variables of type **HttpRequest** and **ILogger** as parameters named *request* and *logger*:

    ```csharp
    public static IActionResult Run(
        HttpRequest request,
        ILogger logger)
    { }
    ```

1. Append an attribute to the **Run** method of type **FunctionNameAttribute** that has its **name** parameter set to a value of **Echo**:

    ```csharp
    [FunctionName("Echo")]
    public static IActionResult Run(
        HttpRequest request,
        ILogger logger)
    { }
    ```

1. Append an attribute to the **request** parameter of type **HttpTriggerAttribute** that has its **methods** parameter array set to a single value of **POST**:

    ```csharp
    [FunctionName("Echo")]
    public static IActionResult Run(
        [HttpTrigger("POST")] HttpRequest request,
        ILogger logger)
    { }
    ```

1. Within the **Run** method, log a fixed message:

    ```csharp
    logger.LogInformation("Received a request");
    ```

1. Finally, echo the body of the HTTP request as the HTTP response:

    ```csharp
    return new OkObjectResult(request.Body);
    ```

1. **Save** the **Echo.cs** file.
#### Task 3: Write Azure Blob Storage code using the Azure SDK for .NET

1. Within the **Run** method of the **FileParser** class, delete the following line of code:

    ```csharp
    return new OkObjectResult(connectionString);
    ```

1. Still within the **Run** method, create a new instance of the **BlobClient** class by passing in your *connectionString* variable, a  ``"drop"`` string value, and a ``"records.json"`` string value to the constructor:

    ```csharp
    BlobClient blob = new BlobClient(connectionString, "drop", "records.json");
    ```

1. Still within the **Run** method, use the **BlobClient.DownloadAsync** method to download the contents of the referenced blob asynchronously and store the result in a variable named *response*:

    ```csharp
    var response = await blob.DownloadAsync();
    ```

1. Still within the **Run** method, return the value of the various content stored in the *content* variable by using the **FileStreamResult** class constructor:

    ```csharp
    return new FileStreamResult(response?.Value?.Content, response?.Value?.ContentType);
    ```

1. **Save** the **Echo.cs** file.
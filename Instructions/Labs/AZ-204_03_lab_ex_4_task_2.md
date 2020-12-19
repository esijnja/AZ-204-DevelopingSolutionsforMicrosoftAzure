#### Task 2: Create a new container by using the SDK

1.  In the **Program** class, create a new **private static** method named **GetContainerAsync** that's asynchronous and has two parameter types, **BlobServiceClient** and **string**:

    ```
    private static async Task<BlobContainerClient> GetContainerAsync(BlobServiceClient client, string containerName)
    {      
    }
    ```

1.  In the **GetContainerAsync** method, get a new instance of the **BlobContainerClient** class by using the **GetBlobContainerClient** method of the **BlobServiceClient** class, passing in the **containerName** parameter. Invoke the **CreateIfNotExistsAsync** method of the **BlobContainerClient** class:

    ```
    BlobContainerClient container = client.GetBlobContainerClient(containerName);
    await container.CreateIfNotExistsAsync(PublicAccessType.Blob);
    ```

1.  In the **GetContainerAsync** method, render the name of the container that was potentially created:

    ```
    await Console.Out.WriteLineAsync($"New Container:\t{container.Name}");
    ```

1.  Return the instance of the **BlobContainerClient** class named **container** as the result of the **GetContainerAsync** method:

    ```
    return container;
    ``` 
    
1.  In the **Main** method, add a new line of code to create a variable named *newContainerName* with a value of **vector-graphics**:

    ```
    string newContainerName = "vector-graphics";
    ```

1.  In the **Main** method, add a new line of code to invoke the **GetContainerAsync** method, passing in the *serviceClient* and *newContainerName* variables as parameters:

    ```
    BlobContainerClient containerClient = await GetContainerAsync(serviceClient, newContainerName);
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\03\\Solution\\BlobManager** folder.

1.  Observe the output from the currently running console application. The updated output includes metadata about the new container and blobs.

1.  Close the current terminal.

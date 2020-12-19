#### Task 1: Enumerate the blobs in an existing container by using the SDK

1.  In the **Program** class, create a new **private static** method named **EnumerateBlobsAsync** that's asynchronous and has two types of parameters, **BlobServiceClient** and **string**:

    ```
    private static async Task EnumerateBlobsAsync(BlobServiceClient client, string containerName)
    {      
    }
    ```

1.  In the **EnumerateBlobsAsync** method, get a new instance of the **BlobContainerClient** class by using the **GetBlobContainerClient** method of the **BlobServiceClient** class, passing in the **containerName** parameter:

    ```
    BlobContainerClient container = client.GetBlobContainerClient(containerName);
    ```

1.  In the **EnumerateBlobsAsync** method, render the name of the container that will be enumerated:

    ```
    await Console.Out.WriteLineAsync($"Searching:\t{container.Name}");
    ```

1.  In the **EnumerateBlobsAsync** method, create an asynchronous **foreach** loop that iterates over the results of an invocation of the **GetBlobsAsync** method of the **BlobContainerClient** class and prints out the name of each blob:

    ```
    await foreach (BlobItem blob in container.GetBlobsAsync())
    {
        await Console.Out.WriteLineAsync($"Existing Blob:\t{blob.Name}");
    }
    ```

1.  In the **Main** method, add a new line of code to create a variable named *existingContainerName* with a value of **raster-graphics**:

    ```
    string existingContainerName = "raster-graphics";
    ```

1.  In the **Main** method, add a new line of code to invoke the **EnumerateBlobsAsync** method, passing in the *serviceClient* and *existingContainerName* variables as parameters:

    ```
    await EnumerateBlobsAsync(serviceClient, existingContainerName);
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\03\\Solution\\BlobManager** folder.

1.  Observe the output from the currently running console application. The updated output includes metadata about the existing container and blobs.

1.  Close the current terminal.
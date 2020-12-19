#### Task 4: Access blob URI by using the SDK

1.  In the **Program** class, create a new **private static** method named **GetBlobAsync** that's asynchronous and has two types of parameters, **BlobContainerClient** and **string**:

    ```
    private static async Task<BlobClient> GetBlobAsync(BlobContainerClient client, string blobName)
    {      
    }
    ```

1.  In the **GetBlobAsync** method, get a new instance of the **BlobClient** class by using the **GetBlobClient** method of the **BlobContainerClient** class, passing in the **blobName** parameter:

    ```
    BlobClient blob = client.GetBlobClient(blobName);
    ```

1.  In the **GetBlobAsync** method, render the name of the blob that was referenced:

    ```
    await Console.Out.WriteLineAsync($"Blob Found:\t{blob.Name}");
    ```

1.  Return the instance of the **BlobClient** class named **blob** as the result of the **GetBlobAsync** method:

    ```
    return blob;
    ```  
    
1.  In the **Main** method, add a new line of code to create a variable named *uploadedBlobName* with a value of **vector-graphics**:

    ```
    string uploadedBlobName = "graph.svg";
    ```

1.  In the **Main** method, add a new line of code to invoke the **GetBlobAsync** method, passing in the *containerClient* and *uploadedBlobName* variables as parameters and store the result in a variable named *blobClient* of type **BlobClient**:

    ```
    BlobClient blobClient = await GetBlobAsync(containerClient, uploadedBlobName);
    ```

1.  In the **Main** method, add a new line of code to render the **Uri** property of the *blobClient* variable:

    ```
    await Console.Out.WriteLineAsync($"Blob Url:\t{blobClient.Uri}");
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\03\\Solution\\BlobManager** folder.

1.  Observe the output from the currently running console application. The updated output includes the final URL to access the blob online. Record the value of this URL to use later in the lab.

    > **Note**: The URL will likely be similar to the following string: **https://mediastor*[yourname]*.blob.core.windows.net/vector-graphics/graph.svg**

1.  Close the current terminal.
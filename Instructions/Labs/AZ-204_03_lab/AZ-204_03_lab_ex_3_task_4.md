#### Task 4: Enumerate the existing containers

1.  In the **Program** class, create a new **private static** method named **EnumerateContainersAsync** that's asynchronous and has a single parameter of type **BlobServiceClient**:

    ```
    private static async Task EnumerateContainersAsync(BlobServiceClient client)
    {        
    }
    ```

1.  In the **EnumerateContainersAsync** method, create an asynchronous **foreach** loop that iterates over the results of an invocation of the **GetBlobContainersAsync** method of the **BlobServiceClient** class and prints out the name of each container:

    ```
    await foreach (BlobContainerItem container in client.GetBlobContainersAsync())
    {
        await Console.Out.WriteLineAsync($"Container:\t{container.Name}");
    }
    ```

1.  In the **Main** method, add a new line of code to invoke the **EnumerateContainersAsync** method, passing in the *serviceClient* variable as a parameter:

    ```
    await EnumerateContainersAsync(serviceClient);
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\03\\Solution\\BlobManager** folder.

1.  Observe the output from the currently running console application. The updated output includes a list of every existing container in the account.

1.  Close the current terminal.

#### Review

In this exercise, you accessed existing containers by using the Storage SDK. #### Task 4: Enumerate the existing containers

1.  In the **Program** class, create a new **private static** method named **EnumerateContainersAsync** that's asynchronous and has a single parameter of type **BlobServiceClient**:

    ```
    private static async Task EnumerateContainersAsync(BlobServiceClient client)
    {        
    }
    ```

1.  In the **EnumerateContainersAsync** method, create an asynchronous **foreach** loop that iterates over the results of an invocation of the **GetBlobContainersAsync** method of the **BlobServiceClient** class and prints out the name of each container:

    ```
    await foreach (BlobContainerItem container in client.GetBlobContainersAsync())
    {
        await Console.Out.WriteLineAsync($"Container:\t{container.Name}");
    }
    ```

1.  In the **Main** method, add a new line of code to invoke the **EnumerateContainersAsync** method, passing in the *serviceClient* variable as a parameter:

    ```
    await EnumerateContainersAsync(serviceClient);
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\03\\Solution\\BlobManager** folder.

1.  Observe the output from the currently running console application. The updated output includes a list of every existing container in the account.

1.  Close the current terminal.

#### Review

In this exercise, you accessed existing containers by using the Storage SDK. 
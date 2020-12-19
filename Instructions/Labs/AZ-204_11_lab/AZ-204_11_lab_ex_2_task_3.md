#### Task 3: Validate Azure Storage access

1.  In the **Main** method, add the following block of code to connect to the storage account and to asynchronously create the queue if it doesn't already exist:

    ```
    QueueClient client = new QueueClient(storageConnectionString, queueName);        
    await client.CreateAsync();
    ```

1.  Still in the **Main** method, add the following block of code to render the Uniform Resource Identifier (URI) of the queue endpoint:

    ```
    Console.WriteLine($"---Account Metadata---");
    Console.WriteLine($"Account Uri:\t{client.Uri}");
    ```

1.  Save the **Program.cs** file.

1.  Using a terminal, run the ASP.NET web application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\11\\Solution\\MessageProcessor** folder.

1.  Observe the output from the currently running console application. The output contains metadata for the queue endpoint.

1.  Close the current terminal.

#### Review

In this exercise, you configured your .NET project to access the Storage service and manipulate a queue made available through the service.
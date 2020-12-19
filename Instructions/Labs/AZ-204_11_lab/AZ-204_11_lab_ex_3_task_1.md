#### Task 1: Write code to access queue messages

1.  In the **Main** method, perform the following actions:

    1.  Render a header by using the **Console.WriteLine** static method:

        ```
        Console.WriteLine($"---Existing Messages---");
        ```
    
    1.  Add the following block of code to create variables that will be used when retrieving queue messages:

        ```
        int batchSize = 10;
        TimeSpan visibilityTimeout = TimeSpan.FromSeconds(2.5d);
        ```

    1.  Add the following block of code to retrieve a batch of messages asynchronously from the queue service and iterate over the messages:

        ```
        Response<QueueMessage[]> messages = await client.ReceiveMessagesAsync(batchSize, visibilityTimeout);
        foreach(QueueMessage message in messages?.Value)
        {
        }
        ```

    1.  Within the **foreach** block, render the **MessageId** and **MessageText** properties of the **[QueueMessage](https://docs.microsoft.com/dotnet/api/azure.storage.queues.models.queuemessage)** instance:

        ```
        Console.WriteLine($"[{message.MessageId}]\t{message.MessageText}");
        ```

1.  Save the **Program.cs** file.

1.  Using a terminal, build the ASP.NET web application project:

    ```
    dotnet build
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\11\\Solution\\MessageProcessor** folder.

1.  Close the current terminal.
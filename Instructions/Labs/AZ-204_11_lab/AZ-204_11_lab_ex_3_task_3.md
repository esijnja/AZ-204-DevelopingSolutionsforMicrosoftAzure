#### Task 3: Delete queued messages

1.  In the **Visual Studio Code** window, open the **Program.cs** file.

1.  Update the **foreach** loop's block of code to invoke the **DeleteMessageAsync** method of the **QueueMessage** class, passing in the **MessageId** and **PopReceipt** properties of the *message* variable:

    ```
    foreach(QueueMessage message in messages?.Value)
    {
        Console.WriteLine($"[{message.MessageId}]\t{message.MessageText}");
        await client.DeleteMessageAsync(message.MessageId, message.PopReceipt);
    }
    ```

1.  **Save** the **Program.cs** file.

1.  Using a terminal, run the ASP.NET web application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\11\\Solution\\MessageProcessor** folder.

1.  Observe the output from the currently running console application. The message that you created earlier in the lab still exists because it hasn't been deleted previously.

1.  Close the current terminal.

1.  In the **Azure Storage Explorer** window, within the **asyncstor*[yourname]*** node for the Storage account that you created earlier in this lab, find and open the **messagequeue** queue.

1.  Observe the empty list of messages in the queue.

    > **Note**: You might need to refresh the queue.

#### Review

In this exercise, you read and deleted existing messages from the Storage queue by using the .NET library.
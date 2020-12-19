#### Task 1: Write code to create queue messages

1.  In the **Visual Studio Code** window, open the **Program.cs** file.

1.  In the **Main** method, perform the following actions:

    1.  Render a header by using the **Console.WriteLine** static method:

        ```
        Console.WriteLine($"---New Messages---");
        ```
    
    1.  Add the following block of code to create a new string variable named *greeting* with a value of **Hi, Developer!**, and then invoke the **SendMessageAsync** method of the **QueueClient** class by using the *greeting* variable as a parameter:

        ```
        string greeting = "Hi, Developer!";
        await client.SendMessageAsync(greeting);
        ```

    1.  Add the following block of code to render the content of the message that you sent:

        ```
        Console.WriteLine($"Sent Message:\t{greeting}");
        ```

1.  **Save** the **Program.cs** file.

1.  Using a terminal, run the ASP.NET web application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\11\\Solution\\MessageProcessor** folder.

1.  Observe the output from the currently running console application. The content of the new message that you sent should be in the output.

1.  Close the current terminal.
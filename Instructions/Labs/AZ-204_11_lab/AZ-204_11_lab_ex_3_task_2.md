#### Task 2: Test message queue access

1.  Using a terminal, run the ASP.NET web application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\11\\Solution\\MessageProcessor** folder.

1.  Observe the output from the currently running console application. The output indicates that no messages are in the queue.

1.  Close the current terminal.

1.  Find the **asyncstor*[yourname]*** Storage account that you created earlier in this lab.

1.  In the **Overview** section of the blade, select **Open in Explorer** to open the Storage account by using Storage Explorer.

1.  In the **Azure Storage Explorer** application, sign in to your Azure account.

1.  From the **Azure Storage Explorer** application, in the **EXPLORER** pane, find and expand the **asyncstor*[yourname]*** storage account that you created earlier in this lab.

1.  Within the **asyncstor*[yourname]*** node for the Storage account that you created earlier in this lab, find and open the **messagequeue** queue.

1.  Add a new message to the queue with the following properties:

    -   Message text: **Hello World**

    -   Expires in: **12 Hours**

    -   Encode message body in Base 64: **No**

1.  Return to the Visual Studio Code application.

1.  Using a terminal, run the ASP.NET web application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\11\\Solution\\MessageProcessor** folder.

1.  Observe the output from the currently running console application. The output includes the new message that you created.

1.  Close the current terminal.
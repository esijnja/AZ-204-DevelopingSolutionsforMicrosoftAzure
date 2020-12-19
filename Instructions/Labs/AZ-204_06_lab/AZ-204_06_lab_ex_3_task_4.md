#### Task 4: Test the updated application

1.  Using a terminal, run the .NET console application project:

    ```
    dotnet run
    ```

    > **Note**: If there are any build errors, review the **Program.cs** file in the **Allfiles (F):\\Allfiles\\Labs\\06\\Solution\\GraphClient** folder.

1.  Observe the message in the output from the currently running console application. Record the value of the code in the message. You'll use this value later in the lab.

1.  Go to <https://microsoft.com/devicelogin>, and then enter the code value that you copied earlier in the lab.

1.  Sign in by using your Microsoft account.

    > **Note**: You might have the option to select an existing Microsoft account as opposed to signing in again.

1.  Close the currently open browser window.

1.  In the **Visual Studio Code** window, observe the output from the Microsoft Graph request in the currently running console application.

1.  Close the current terminal.

#### Review

In this exercise, you queried Microsoft Graph by using the SDK and MSAL-based authentication.
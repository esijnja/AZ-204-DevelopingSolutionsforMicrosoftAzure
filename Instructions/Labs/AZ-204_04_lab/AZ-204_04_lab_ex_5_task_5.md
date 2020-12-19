#### Task 5: Validate that the .NET application successfully connects to Azure Cosmos DB

1.  Using a terminal, change your context to the **AdventureWorks.Web** folder:

    ```
    cd .\AdventureWorks.Web\
    ```
    
1.  Using the same terminal, run the ASP.NET web application project:

    ```
    dotnet run
    ```

    > **Note**: The **dotnet run** command will automatically build any changes to the project and then start the web application without a debugger attached. The command will output the URL of the running application and any assigned ports.

1.  Open the Microsoft Edge browser.

1.  In the open browser window, browse to the web application that's hosted at **localhost** on port **5000**.

    > **Note**: The URL is <http://localhost:5000>.

1.  In the web application, observe the list of models displayed from the front page.

1.  Find the **Touring-1000** model, and then select **View Details**.

1.  From the **Touring-1000** product detail page, perform the following actions:

    1.  In the **Select options** list, select **Touring-1000 Yellow, 50, $2,384.07**.
    
    1.  Find **Add to Cart**.

1.  Close the browser window displaying your web application.

1.  Return to the **Visual Studio Code** window.

1.  Close the current terminal.

#### Review

In this exercise, you wrote C# code to query an Azure Cosmos DB collection by using the .NET SDK.

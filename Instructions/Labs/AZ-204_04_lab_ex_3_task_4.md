#### Task 4: Validate the web application

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

1.  Find the **Water Bottle** model, and then select **View Details**.

1.  From the **Water Bottle** product detail page, find **Add to Cart**, and then observe that the checkout functionality is currently disabled.

1.  Close the browser window that's displaying your web application.

1.  Return to the **Visual Studio Code** window.

1.  Close the current terminal.

#### Review

In this exercise, you configured your ASP.NET web application to connect to your resources in Azure.
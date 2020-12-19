#### Task 4: Use an imported SQL database

1.  Go back to the blade for the **polysqlsrvr*[yourname]*** SQL server resource.

1.  Open the Firewalls and virtual networks pane.

1.  Add your current client IP address to the list of allowed IP addresses, and then save the list.

1.  Go to the blade for the **AdventureWorks** SQL database resource that you recently imported.

1.  Open the Connection strings pane, and then record the value of the **ADO.NET (SQL Authentication)** connection string. 

1.  Update the connection string that you recorded by replacing the placeholder values for *your_username* and *your_password*

    > **Note**: For example, if your connection string was originally ``Server=tcp:polysqlsrvrinstructor.database.windows.net,1433;Initial Catalog=AdventureWorks;User ID={your_username};Password={your_password};``, your updated connection string will be ``Server=tcp:polysqlsrvrinstructor.database.windows.net,1433;Initial Catalog=AdventureWorks;User ID=testuser;Password=TestPa55w.rd;``

1.  Go back to the blade for the **AdventureWorks** SQL database resource.

1.  Open the Query editor pane, and then sign in by using the following credentials:

    -   Username: **testuser**

    -   Password: **TestPa55w.rd**

1.  Run the following query, and then observe the results:

    ```
    SELECT * FROM AdventureWorks.dbo.Models
    ```

    > **Note**: This query will return a list of models from the home page of the web application.

1.  Run this additional query, and then observe the results:

    ```
    SELECT * FROM AdventureWorks.dbo.Products
    ```

    > **Note**: This query will return a list of products that are associated with each model.

#### Review

In this exercise, you imported all the resources that you'll use with your web application.
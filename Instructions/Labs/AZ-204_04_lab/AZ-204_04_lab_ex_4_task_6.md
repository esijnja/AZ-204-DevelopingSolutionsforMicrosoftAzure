#### Task 6: Validate the migration

1.  Return to the **Microsoft Edge** browser window with the Azure portal.

1.  Go to the blade for the **polycosmos*[yourname]*** Azure Cosmos DB account that you created earlier in this lab.

1.  Open the Data Explorer pane.

1.  Create a new **SQL query** tab within the context of the **Retail** database and **Online** container.

1.  Run the following query, and then observe the results:

    ```
    SELECT * FROM models
    ```

1.  Run the following query, and then observe the results:

    ```
    SELECT VALUE COUNT(1) FROM models
    ```

#### Review

In this exercise, you used Entity Framework and the .NET SDK for Azure Cosmos DB to migrate data from SQL Database to Azure Cosmos DB.
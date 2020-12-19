#### Task 3: Create an Azure Cosmos DB account resource

1.  Create a new **Azure Cosmos DB** instance with the following details:
    
    -   Account name: **polycosmos*[yourname]***

    -   Existing resource group: **PolyglotData**

    -   API: **Core (SQL)**
    
    -   Notebooks (Preview): **Off**

    -   Apply Free Tier Discount: **Do Not Apply**

    -   Location: **(US) East US**

    -   Account Type **Non-Production**

    -   Multi-region writes: **Disable**

    > **Note**: Wait for Azure to finish creating the Azure Cosmos DB account before you move forward with the lab. You'll receive a notification when the Azure Cosmos DB account is created.

1.  Go to the blade for your newly created Azure Cosmos DB account resource, and then open the Keys pane.

1.  In the Keys pane, record the value of the **PRIMARY CONNECTION STRING** text box. 

    > **Note**: You'll use these values later in this lab.
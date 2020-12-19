#### Task 2: Create a Storage account

1.  Create a new storage account with the following details:
    
    -   New resource group: **AsyncProcessor**

    -   Name: **asyncstor*[yourname]***

    -   Location: **(US) East US**

    -   Performance: **Standard**

    -   Account kind: **StorageV2 (general purpose v2)**

    -   Replication: **Locally-redundant storage (LRS)**

    -   Access tier: **Hot**

    > **Note**: Wait for Azure to finish creating the storage account before you move forward with the lab. You'll receive a notification when the account is created.

1.  Find the **Access Keys** blade of your newly created storage account instance.

1.  Record the value of the **Connection string** text box. You'll use this value later in this lab.

#### Review

In this exercise, you created a new Storage account that you'll use through the remainder of the lab.
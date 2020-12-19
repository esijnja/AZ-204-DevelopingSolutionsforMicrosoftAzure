#### Task 2: Create an Azure Storage account

1. Create a new storage account with the following details:
    - New resource group: **ConfidentialStack**
    - Name: **securestor[yourname]**
    - Location: **East US**
    - Performance: **Standard**
    - Account kind: **StorageV2 (general purpose v2)**
    - Replication: **Locally-redundant storage (LRS)**
    - Access tier: **Hot**
    > **Note**: Wait for Azure to finish creating the storage account before you move forward with the lab. You'll receive a notification when the account is created.
1. Open the **Access Keys** blade of your newly created storage account instance.
1. Record the value in the **Connection string** text box. You'll use this value later in this lab.
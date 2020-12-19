#### Task 2: Create an Application Insights resource

1.  Create a new Application Insights account with the following details:
    
    -   New resource group: **MonitoredAssets**

    -   Name: **instrm*[yourname]***

    -   Region: **(US) East US**
    
    -   Resource Mode: **Classic**

    > **Note**: Wait for Azure to finish creating the storage account before you move forward with the lab. You'll receive a notification when the account is created.

1.  Access the **Properties** section of the **Application Insights** blade.

1.  Get the value of the **Instrumentation Key** text box. This key is used by client applications to connect to Application Insights.
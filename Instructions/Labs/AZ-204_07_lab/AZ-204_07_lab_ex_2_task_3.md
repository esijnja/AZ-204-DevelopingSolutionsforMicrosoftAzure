#### Task 3: Configure a Key Vault access policy

1. Access the **securevault[yourname]** key vault that you created earlier in this lab.
1. Browse to the **Access Policies** link in the **Settings** section.
1. Create a new access policy with the following settings:
    - Principal: **securefunc[yourname]**
        > **Note**: The system-assigned managed identity you created earlier in this lab will have the same name as the Azure Functions resource.
    - Key permissions: **None**
    - Secret permissions: **GET**
    - Certificate permissions: **None**
    - Authorized application: **None**
1. Save your changes to the list of **Access Policies**.
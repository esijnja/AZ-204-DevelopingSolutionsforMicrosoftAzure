#### Task 2: Create a Key Vault secret

1. Access the **securevault[yourname]** key vault that you created earlier in this lab.
1. Select the **Secrets** link in the **Settings** section.
1. Create a new secret with the following settings:
    - Name: **storagecredentials**
    - Value: ***Storage connection string***
    - Enabled: **Yes**
    > **Note**: Use the storage account connection string that you recorded earlier in this lab for the value of this secret.
1. Select through the secret to find the metadata for its latest version.
1. Record the value of the **Secret Identifier** text box because you'll use this later in the lab.
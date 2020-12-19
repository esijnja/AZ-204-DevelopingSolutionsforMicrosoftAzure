#### Task 4: Create a Key Vault-derived application setting

1. Access the **securefunc[yourname]** function app that you created earlier in this lab.
1. Browse to the **Configuration** option from the **Settings** section.
1. Create a new application setting by using the following details:
    - Name: **StorageConnectionString**
    - Value: **@Microsoft.KeyVault(SecretUri=*Secret Identifier*)**
    - Deployment slot setting: **Not selected**
    > **Note**: You'll need to build a reference to your ***Secret Identifier*** by using the previous syntax. For example, if your ***Secret Identifier*** is ``https://securevaultstudent.vault.azure.net/secrets/storagecredentials/17b41386df3e4191b92f089f5efb4cbf``, your value would be ``@Microsoft.KeyVault(SecretUri=https://securevaultstudent.vault.azure.net/secrets/storagecredentials/17b41386df3e4191b92f089f5efb4cbf)``.
1. Save your changes to the application settings.

> **Review**: In this exercise, you created a system-assigned managed service identity for your function app and then gave that identity the appropriate permissions to get the value of a secret in your key vault. Finally, you created a secret that you referenced within your function app's configuration settings.
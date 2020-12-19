#### Task 6: Test the Key Vault-derived application setting

1. Sign in to the Azure portal (<https://portal.azure.com>).
1. Access the **securefunc[yourname]** function app that you created earlier in this lab.
1. From the **App Service** blade, locate and open the **Functions** section, and then locate and open the **FileParser** function.
1. In the **Function** blade, select the **Code + Test** option from the **Developer** section.
1. In the function editor, select **Test/Run**.
1. In the pop-up dialog that appears, perform the following actions:
    - In the **HTTP method** list, select **GET**.
1. Select **Run** to test the function.
1. Observe the result of the test run. The result should be your Azure Storage connection string.

> **Review**: In this exercise, you used a service identity to read the value of a secret stored in Key Vault and returned that value as the result of a function app.
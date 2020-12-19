#### Task 4: Deploy and validate the Azure Functions app

1. Open the **Windows Terminal** application.
1. Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\07\\Starter\\func** project directory.
1. Log in to the Azure CLI by using your Azure credentials:

    ```powershell
    az login
    ```

1. Publish the function app project again:

    ```powershell
    func azure functionapp publish <function-app-name>
    ```

    > **Note**: As an example, if your **Function App name** is **securefuncstudent**, your command would be ``func azure functionapp publish securefuncstudent``. You can review the documentation to [publish the local function app project][azure-functions-core-tools-publish-azure] using the **Azure Functions Core Tools**.
1. Wait for the deployment to finalize before you move forward with the lab.
1. Close the currently running **Windows Terminal** application.
1. Sign in to the Azure portal (<https://portal.azure.com>).
1. Access the **securefunc[yourname]** function app that you created earlier in this lab.
1. From the **App Service** blade, locate and open the **Functions** section, then locate and open the **FileParser** function.
1. In the **Function** blade, select the **Code + Test** option from the **Developer** section.
1. In the function editor, select **Test/Run**.
1. In the pop-up dialog that appears, perform the following actions:
    - In the **HTTP method** list, select **GET**.
1. Select **Run** to test the function.
1. Observe the results of the test run. The output will contain the content of the **$/drop/records.json** blob stored in your Azure Storage account.

> **Review**: In this exercise, you used C\# code to access a storage account and then downloaded the contents of a blob.
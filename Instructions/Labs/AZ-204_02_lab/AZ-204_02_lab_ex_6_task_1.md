#### Task 1: Deploy using the Azure Functions Core Tools

1. Open the **Windows Terminal** application.
1. Change the current directory to the **Allfiles (F):\\Allfiles\\Labs\\02\\Starter\\func** project directory.
1. Log in to the Azure Command-Line Interface (CLI) by using your Azure credentials:

    ```powershell
    az login
    ```

1. Publish the function app project:

    ```powershell
    func azure functionapp publish <function-app-name>
    ```

    > **Note**: For example, if your **Function App name** is **funclogicstudent**, your command would be ``func azure functionapp publish funclogicstudent``. You can review the documentation to [publish the local function app project][azure-functions-core-tools-publish-azure] using the **Azure Functions Core Tools**.
1. Wait for the deployment to finalize before you move forward with the lab.
1. Close the currently running **Windows Terminal** application.
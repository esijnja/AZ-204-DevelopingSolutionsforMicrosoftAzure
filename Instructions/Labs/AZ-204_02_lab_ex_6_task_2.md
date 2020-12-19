#### Task 2: Validate deployment

1. Sign in to the Azure portal (<https://portal.azure.com>).
1. Access the **funclogic[yourname]** function app that you created earlier in this lab.
1. From the **App Service** blade, locate and open the **Functions** section, then locate and open the **GetSettingInfo** function.
1. In the **Function** blade, select the **Code + Test** option from the **Developer** section.
1. In the function editor, select **Test/Run**.
1. In the popup dialog that appears, perform the following actions:
    - In the **HTTP method** list, select **GET**.
1. Select **Run** to test the function.
1. Observe the results of the test run. the JSON content should be the same as the **settings.json** file.

> **Review**: In this exercise, you deployed a local function project to Azure Functions and validated that the functions work in Azure.
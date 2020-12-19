#### Task 3: Create a web app by using Azure App Services resource

1.  Create a new **web app** with the following details:

    -   Existing resource group: **MonitoredAssets**
    
    -   Web App name: ***smpapi\***[yourname]***

    -   Publish: **Code**

    -	Runtime stack: **.NET Core 3.1 (LTS)**

    -	Operating System: **Windows**

    -	Region: **East US**

    -	New App Service plan: **MonitoredPlan**
    
    -	SKU and size: **Standard (S1)**

    -	Application Insights: **Enabled**

    -	Existing Application Insights resource: **instrm*[yourname]***
  
    > **Note**: Wait for Azure to finish creating the web app before you move forward with the lab. You'll receive a notification when the app is created.

1.  Access the web app with a prefix of **smpapi\*** that you created earlier in this lab.

1.  In the **Settings** section, go to the **Configuration** section.

1.  Find and access the **Application Settings** tab in the **Configuration** section.

1.  Get the value corresponding to the **APPINSIGHTS\_INSTRUMENTATIONKEY** application settings key. This value was set automatically when you built your web app.

1.  Access the **Properties** section of the **App Service** blade.

1.  Record the value of the **URL** text box. You'll use this value later in the lab to make requests against the API.
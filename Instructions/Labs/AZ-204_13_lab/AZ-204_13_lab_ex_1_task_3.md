#### Task 3: Create a web app by using Azure App Service

1.  Create a new web app with the following details:

    -   Existing resource group: **MarketingContent**
    
    -   Name: **landingpage*[yourname]***

    -   Publish: **Docker Container**

    -	Operating system: **Linux**

    -	Region: **East US**

    -	New App Service plan: **MarketingPlan**
    
    -	SKU and size: **Premium V2 P1v2**

    -	Docker options: **Single Container**

    -	Image source: **Docker Hub**

    -   Access type: **Public**

    -   Image and tag: **microsoftlearning/edx-html-landing-page:latest**
  
    > **Note**: Wait for Azure to finish creating the web app before you move forward with the lab. You'll receive a notification when the app is created.

1.  Access the **landingpage*[yourname]*** web app that you created earlier in this lab.

1.  In the **Settings** section, go to the **Properties** section, and then record the value of the **URL** text box. You'll use this value later in the lab.

#### Review

In this exercise, you created an Azure Storage account and an Azure Web App that you'll use later in this lab.
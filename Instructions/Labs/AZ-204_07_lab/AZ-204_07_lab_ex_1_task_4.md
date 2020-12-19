#### Task 4: Create an Azure Functions app

1. Create a new function app with the following details:
    - Existing resource group: **ConfidentialStack**
    - App name: **securefunc[yourname]**
    - Publish: **Code**
    - Runtime Stack: **.NET Core**
    - Version: **3.1**
    - Region: **East US**
    - Operating system: **Linux**
    - Storage account: **securestor[yourname]**
    - Plan: **Consumption (Serverless)**
    - Enable Application Insights: **Yes**

    > **Note**: Wait for Azure to finish creating the function app before you move forward with the lab. You'll receive a notification when the app is created.

> **Review**: In this exercise, you created all the resources that you'll use for this lab.
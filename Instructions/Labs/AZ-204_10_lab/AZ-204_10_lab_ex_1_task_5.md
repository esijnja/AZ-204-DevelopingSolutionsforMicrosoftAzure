#### Task 5: Deploy the Azure Event Grid viewer to a web app

1.  Create a new web app with the following details:

    -   Existing resource group: **PubSubEvents**
    
    -   Name: **eventviewer*[yourname]***

    -   Publish: **Docker Container**

    -	Operating system: **Linux**

    -	Region: **East US**

    -	New App Service plan: **EventPlan**
    
    -	SKU and size: **Premium V2 P1v2**

    -	Docker options: **Single Container**

    -	Image source: **Docker Hub**

    -   Access type: **Public**

    -   Image and tag: **microsoftlearning/azure-event-grid-viewer:latest**
  
    > **Note**: Wait for Azure to finish creating the web app before you continue with the lab. You'll receive a notification when the app is created.

#### Review

In this exercise, you created the Event Grid topic and web app that you will use throughout the remainder of the lab.
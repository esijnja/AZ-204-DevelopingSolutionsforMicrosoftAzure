#### Task 2: Create a web app by using Azure App Service resource by using an httpbin container image

1.  Create a new web app with the following details:

    -   New resource group: **ApiService**
    
    -   Name: **httpapi*[yourname]***

    -   Publish: **Docker Container**

    -	Operating system: **Linux**

    -	Region: **East US**

    -	New App Service plan: **ApiPlan**
    
    -	SKU and size: **Premium V2 P1v2**

    -	Docker options: **Single Container**

    -	Image source: **Docker Hub**

    -   Access type: **Public**

    -   Image and tag: **kennethreitz/httpbin:latest**
  
    > **Note**: Wait for Azure to finish creating the web app before you move forward with the lab. You'll receive a notification when the app is created.
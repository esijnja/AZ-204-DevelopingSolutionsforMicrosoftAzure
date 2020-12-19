#### Task 3: Configure Web App settings

1.  Access the **landingpage*[yourname]*** web app that you created earlier in this lab.

1.  In the **Settings** section, go to the **Configuration** section.

1.  Find and access the **Application Settings** tab in the **Configuration** section.

1.  Create a new application setting by using the following details:
    
    -	Name: **CDNMediaEndpoint**

    -	Value: The **URI** value of the **media** container in the **contenthost*[yourname]*** storage account that you recorded earlier in this lab.
    
    -	Deployment slot setting: **Not selected**

1.  Create a new application setting by using the following details:
    
    -	Name: **CDNVideoEndpoint**

    -	Value: The **URI** value of the **video** container in the **contenthost*[yourname]*** storage account that you recorded earlier in this lab.
    
    -	Deployment slot setting: **Not selected**

1.  Save your changes to the application settings.
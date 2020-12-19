#### Task 5: Deploy a Docker container image to Container Registry

1.  Change the active directory to **\~/clouddrive/ipcheck**.

1.  Use the **dir** command to get the contents of the current directory.

    > **Note**: You'll know that you're in the correct directory if both the **Program.cs** and **Dockerfile** files that you edited earlier in this lab are there.

1.  Use the following command to upload the source code to your container registry and build the container image as a  Container Registry task:

    ```
    az acr build --registry $acrName --image ipcheck:latest .
    ``` 

    > **Note**: Wait for the build task to complete before moving forward with this lab.

1.  Close the Cloud Shell pane.
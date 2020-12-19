#### Task 1: Upload a sample Storage blob

1. Access the **securestor[yourname]** storage account that you created earlier in this lab.
1. Select the **Containers** link in the **Blob service** section, and then create a new container with the following settings:
    - Name: **drop**
    - Public access level: **Blob (anonymous read access for blobs only)**
1. Browse to the new **drop** container, and then select **Upload** to upload the **records.json** file in the **Allfiles (F): \\Allfiles\\Labs\\07\\Starter** folder on your lab VM.
    > **Note:** You should enable the **Overwrite if files already exist** option.
1. Find the metadata for the **records.json** blob by selecting the blob entry in the list of blobs.
1. Using a new browser tab, go to to the URL for the blob, and then find the blob’s contents.
1. Update the container’s access level by changing the **Public access level** to **Private (no anonymous access)**.
1. Using a new browser window or tab, go to to the URL for the blob, and then find the blob’s contents. You should receive an error message indicating that the resource wasn't found.
    > **Note**: If you don't receive the error message, your browser might have cached the file. Refresh the page until you receive the error message.
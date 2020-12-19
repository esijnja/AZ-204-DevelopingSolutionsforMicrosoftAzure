#### Task 2: Automatically deploy a container image to an Azure container instance

1.  Select the **Repositories** link to find your images in the registry.

1.  Select the **ipcheck** image, and then find the **latest** tag for that image.

1.  Right-click the **latest** tag or activate the shortcut menu for the **ipcheck** container image to **"run"** a new Azure container instance with the following settings:
    
    -	Container name: **managedcompute**

    -	OS type: **Linux**

    -	Resource group: **ContainerCompute**

    -	Location: **East US**

    -	Number of cores: **2**

    -	Memory (GB): **4**

    -	Public IP address: **No** 

    > **Note**: Wait for the creation task to complete before moving on with this lab.
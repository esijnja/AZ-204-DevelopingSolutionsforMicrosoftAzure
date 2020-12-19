#### Task 4: Open Azure Cloud Shell and store Container Registry metadata

1.  Open a new Cloud Shell instance.

1.  At the **Cloud Shell** command prompt, use the **az acr list** command to get a list of all container registries in your subscription.

1.  Use the following command to output the name of the most recently created container registry:

    ```
    az acr list --query "max_by([], &creationDate).name" --output tsv
    ```

1.  Use the following command to save the name of the most recently created container registry in a Bash shell variable named *acrName*:

    ```
    acrName=$(az acr list --query "max_by([], &creationDate).name" --output tsv)
    ```

1.  Use the following script to render the value of the Bash shell variable *acrName*:

    ```
    echo $acrName
    ```
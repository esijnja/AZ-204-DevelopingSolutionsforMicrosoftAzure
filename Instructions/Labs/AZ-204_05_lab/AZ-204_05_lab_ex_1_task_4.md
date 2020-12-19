#### Task 4: Use the Azure CLI commands

1.  Use the **az** command with the **\-\-help** flag to find a list of subgroups and commands at the root level of the CLI.

1.  Use the **az vm** command with the **\-\-help** flag to find a list of subgroups and commands for Azure Virtual Machines:

1.  Use the **az vm create** command with the **\-\-help** flag to find a list of arguments and examples for the **Create Virtual Machine** command:

1.  Use the **az vm create** command to create a new VM with the following settings:
    
    -	Resource group: **ContainerCompute**

    -	Name: **quickvm**

    -	Image: **Debian**

    -	Username: **student**

    -	Password: **StudentPa55w.rd** 

    > **Note**: Wait for the VM creation process to complete. After the process completes, the command will return a JavaScript Object Notation (JSON) file with details about the machine.

1.  Use the **az vm show** command to find a more detailed JSON file that contains various metadata about the newly created VM.

1.  Use the **az vm list-ip-addresses** command to list all the IP addresses associated with the VM:

    ```
    az vm list-ip-addresses --resource-group ContainerCompute --name quickvm
    ```

1.  Use the **az vm list-ip-addresses** command and the **\-\-query** argument to filter the output to only return the first IP address value:

    ```
    az vm list-ip-addresses --resource-group ContainerCompute --name quickvm --query '[].{ip:virtualMachine.network.publicIpAddresses[0].ipAddress}' --output tsv
    ```

1.  Use the following script to store the results of the previous command in a new Bash shell variable named *ipAddress*:

    ```
    ipAddress=$(az vm list-ip-addresses --resource-group ContainerCompute --name quickvm --query '[].{ip:virtualMachine.network.publicIpAddresses[0].ipAddress}' --output tsv)
    ```

1.  Use the following script to render the value of the Bash shell variable *ipAddress*:

    ```
    echo $ipAddress
    ```

1.  Use the following script to connect to the VM that you created earlier in this lab by using the Secure Shell (SSH) tool and the IP address stored in the Bash shell variable *ipAddress*:

    ```
    ssh student@$ipAddress
    ```

1.  During the connection process, you'll receive a warning that the authenticity of the host can't be verified. Continue connecting to the host. Finally, use the password **StudentPa55w.rd** when prompted for credentials

1.  After connecting to the VM, use the following command to get information about the machine to ensure that you're connected to the correct VM:

    ```
    uname -a
    ```

1.  Use the **exit** command to end your SSH session:

    ```
    exit
    ```

1.  Close the Cloud Shell pane.

#### Review

In this exercise, you used Cloud Shell to create a VM as part of an automated script.
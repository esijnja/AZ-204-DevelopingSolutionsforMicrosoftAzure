#### Task 2: Register the Microsoft.CDN provider

1.  Use the **az** command with the **\-\-help** flag to find a list of subgroups and commands at the root level of the Azure CLI.

1.  Use the **az provider** command with the **\-\-help** flag to get a list of commands available for resource providers.

1.  Use the **az provider list** command to list all currently registered providers.

1.  Use the **az provider list** command again with the **\-\-query "[].namespace"** flag to list just the namespaces of the currently registered providers.

1.  Observe the list of currently registered providers. The **Microsoft.CDN** provider isn't currently in the list of providers.

1.  Use the **az provider register** command with the **\-\-help** flag to get the required flags to register a new provider.

1.  Use the **az provider register** command to register a namespace with your current subscription by using the following setting:

    -   Namespace: **Microsoft.CDN**

1.  Close the Cloud Shell pane.
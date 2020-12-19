#### Task 4: Configure web app autoscale options

1.  Go to the **Scale out** section of the **App Services** blade.

1.  In the **Scale out** section, enable **Custom autoscale** with the following details:
    
    -   Name: **ComputeScaler**
    
    -   In the **Scale mode** section, select **Scale based on a metric**.
    
    -   Minimum instances: **2**
    
    -   Maximum instances: **8**
    
    -   Default instances: **3**
    
    -   Scale rules: **Single scale-out rule with default values**

1.  Save your changes to the **autoscale** configuration.

#### Review

In this exercise, you created the resources that you'll use for the remainder of the lab.
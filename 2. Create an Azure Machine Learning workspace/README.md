# Create an Azure Machine Learning Workspace

In this quickstart, you'll create a workspace and then add compute resources to the workspace. You'll then have everything you need to get started with Azure Machine Learning.  

The workspace is the top-level resource for your machine learning activities, providing a centralized place to view and manage the artifacts you create when you use Azure Machine Learning. The compute resources provide a pre-configured cloud-based environment you can use to train, deploy, automate, manage, and track machine learning models.


## Prerequisites

- An Azure account with an active subscription. Complete the first tutorial [Create an account for free](https://github.com/joaosalvadoMicrosoft/Tutorial_create_AML/blob/master/1.%20Create%20an%20Azure%20account/README.md).

## Create the workspace

We will create now the Azure Machine Learning workspace:

Sign in to the [Azure portal](https://portal.azure.com/) by using the credentials for your Azure subscription.

1. In the upper-left corner of the Azure portal, select the three bars, then **+ Create a resource**.

![GitHub Logo](/Images/create_resource.png)

1. Use the search bar to find **Machine Learning**.

1. Select **Machine Learning**.

![GitHub Logo](/Images/create_aml.png)

1. In the **Machine Learning** pane, select **Create** to begin.

1. Provide the following information to configure your new workspace:

   Field|Description
   ---|---
   Workspace name |Enter a unique name that identifies your workspace. In this example, we use **docs-ws**. Names must be unique across the resource group. Use a name that's easy to recall and to differentiate from workspaces created by others.
   Subscription |Select the Azure subscription that you want to use.
   Resource group | Use an existing resource group in your subscription, or enter a name to create a new resource group. A resource group holds related resources for an Azure solution. In this example, we use **docs-aml**. 
   Location | Select the location closest to your users and the data resources to create your workspace.

1. After you're finished configuring the workspace, select **Review + Create**.
1. Select **Create** to create the workspace.


   > It can take several minutes to create your workspace in the cloud.

   When the process is finished, a deployment success message appears.
 
 1. To view the new workspace, select **Go to resource**.
 1. From the portal view of your workspace, select **Launch studio** to go to the Azure Machine Learning studio. 

![GitHub Logo](/Images/launch_studio.png)




## <a name="instance"></a> Create compute instance

You could install Azure Machine Learning on your own computer.  But in this quickstart, you'll create an online compute resource that has a development environment already installed and ready to go.  You'll use this online machine, a *compute instance*, for your development environment to write and run code in Python scripts and Jupyter notebooks.

Create a *compute instance* to use this development environment for the rest of the tutorials and quickstarts.

1. If you didn't select **Go to workspace** in the previous section, sign in to [Azure Machine Learning studio](https://ml.azure.com) now or use the launch studio from previos step, and select your workspace.
1. On the left side, select **Compute**.
1. Select **+New** to create a new compute instance.
1. Supply a name, Keep all the defaults on the first page.
1. Select **Create**.
 
In about two minutes, you'll see the **State** of the compute instance change from *Creating* to *Running*.  It's now ready to go.  

## <a name="cluster"></a> Create compute clusters (optional)

In the tutorial you will only use compute instances but usually in Machine learning projects you use compute clusters to submit jobs and as so this step is optional.
Clusters allow you to distribute a training or batch inference process across a cluster of CPU or GPU compute nodes in the cloud.

Create a compute cluster that will autoscale between zero and four nodes:

1. Still in the **Compute** section, in the top tab, select **Compute clusters**.
1. Select **+New** to create a new compute cluster.
1. Keep all the defaults on the first page, select **Next**.
1. Name the cluster **cpu-cluster**.  If this name already exists, add your initials to the name to make it unique.
1. Leave the **Minimum number of nodes** at 0.
1. Change the **Maximum number of nodes** to 4 if possible.  Depending on your settings, you may have a smaller limit.
1. Change the **Idle seconds before scale down** to 2400.
1. Leave the rest of the defaults, and select **Create**.

In less than a minute, the **State** of the cluster will change from *Creating* to *Succeeded*.  The list shows the provisioned compute cluster, along with the number of idle nodes, busy nodes, and unprovisioned nodes.  Since you haven't used the cluster yet, all the nodes are currently unprovisioned. 

> When the cluster is created, it will have 0 nodes provisioned. The cluster *does not* incur costs until you submit a job. This cluster will scale down when it has been idle for 2,400 seconds (40 minutes).  

## <a name="studio"></a> Quick tour of the studio

The studio is your web portal for Azure Machine Learning. This portal combines no-code and code-first experiences for an inclusive data science platform.

Review the parts of the studio on the left-hand navigation bar:

* The **Author** section of the studio contains multiple ways to get started in creating machine learning models.  You can:

    * **Notebooks** section allows you to create Jupyter Notebooks, copy sample notebooks, and run notebooks and Python scripts.
    * **Automated ML** steps you through creating a machine learning model without writing code.
    * **Designer** gives you a drag-and-drop way to build models using prebuilt modules.

* The **Assets** section of the studio helps you keep track of the assets you create as you run your jobs.  If you have a new workspace, there's nothing in any of these sections yet.

* You already used the **Manage** section of the studio to create your compute resources.  This section also lets you create and manage  data and external services you link to your workspace.  


![GitHub Logo](/Images/aml_quick.png)



### Stop compute instance

If you're not going to use it now, stop the compute instance:

1. In the studio, on the left, select **Compute**.
1. In the top tabs, select **Compute instances**
1. Select the compute instance in the list.
1. On the top toolbar, select **Stop**.



Congratulations! With a few steps, you deployed an Azure Machine learning workspace. Now let's test the notebooks.


Next hands on Lab:
[Access the notebooks](https://github.com/joaosalvadoMicrosoft/Tutorial_create_AML/blob/master/3.%20Access%20the%20notebooks/README.md)


# Access the notebooks


After having created the Azure Machine Learning workspace you should be able to access the notebook from the AML Studio.
In this tutorial, you will run your first Python script in the cloud with Azure Machine Learning. 


This tutorial avoids the complexity of training a machine learning model. You will run a simple "Hello World" Python script in the cloud. 


## Prerequisites

- Complete first this [Create an Azure Machine Learning workspace](https://github.com/joaosalvadoMicrosoft/Tutorial_create_AML/blob/master/2.%20Create%20an%20Azure%20Machine%20Learning%20workspace/README.md) to create a workspace and a compute instance to use in this tutorial series.

## Create and run a Python script

This tutorial will use the compute instance as your development computer.  First create a few folders and the script:

1. Sign in to the [Azure Machine Learning studio](https://ml.azure.com) and select your workspace if prompted.
1. On the left, select **Notebooks**
1. In the **Files** toolbar, select **+**, then select **Create new folder**.
![GitHub Logo](/Images/folder.png)
1. Name the folder **get-started**.
1. To the right of the folder name, use the **...** to create another folder under **get-started**.
![GitHub Logo](/Images/get.png)
1. Name the new folder **src**.  Use the **Edit location** link if the file location is not correct.
1. To the right of the **src** folder, use the **...** to create a new file in the **src** folder. 
1. Name your file *hello.ipynb*.  

Copy this code into your file:

```python
print("Hello world !")
```


### <a name="test"></a>Test your notebook

You can run your code locally, which in this case means on the compute instance. Running code locally has the benefit of interactive debugging of code.  

If you have previously stopped your compute instance, start it now with the **Start compute** tool to the right of the compute dropdown. Wait about a minute for state to change to  *Running*.



To run the code you can click on **Run Cell** or select the cell and click shift+Enter.


You'll see the output of the script in the terminal window bellow. You can click stop the compute to close the session.



Congratulations you have now completed the first part of the Hands-on with Machine Learning.

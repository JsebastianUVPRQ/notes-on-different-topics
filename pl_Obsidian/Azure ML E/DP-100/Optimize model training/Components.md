**Components** allow you to create reusable scripts that can easily be shared across users within the same Azure Machine Learning workspace. You can also use components to build an Azure Machine Learning [[pipeline]].

## Use a component

There are two main reasons why you'd use components:

- To build a pipeline.
- To share ready-to-go code.

You'll want to create components when you're _preparing your code for scale_. When you're done with experimenting and developing, and ready to move your model to production.

Within Azure Machine Learning, you can create a component to store code (in your preferred language) within the workspace. Ideally, you design a component to perform a specific action that is relevant to your machine learning workflow.

For example, a component may consist of a Python script that normalizes your data, trains a machine learning model, or evaluates a model.

Components can be easily shared to other Azure Machine Learning users, who can reuse components in their own Azure Machine Learning pipelines.

![Screenshot of available components in the Azure Machine Learning workspace.](https://learn.microsoft.com/en-us/training/wwl-azure/run-pipelines-azure-machine-learning/media/01-01-components.png)

## Create a component

A component consists of three parts:

- **Metadata**: Includes the component's name, version, etc.
- **Interface**: Includes the expected input parameters (like a dataset or hyperparameter) and expected output (like metrics and artifacts).
- **Command, code and environment**: Specifies how to run the code.

To create a component, you need two files:

- A script that contains the workflow you want to execute.
- A YAML file to define the metadata, interface, and command, code, and environment of the component.

You can create the YAML file, or use the `command_component()` function as a decorator to create the YAML file.
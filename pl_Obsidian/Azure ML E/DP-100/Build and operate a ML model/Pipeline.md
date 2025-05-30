In Azure Machine Learning, a **pipeline** is a workflow of machine learning tasks in which each task is defined as a **component**.

Components can be arranged sequentially or in parallel, enabling you to build sophisticated flow logic to orchestrate machine learning operations. Each component can be run on a specific compute target, making it possible to combine different types of processing as required to achieve an overall goal.

A pipeline can be executed as a process by running the pipeline as a **pipeline job**. Each component is executed as a **child job** as part of the overall pipeline job.

## Build a pipeline

An Azure Machine Learning pipeline is defined in a YAML file. The YAML file includes the pipeline job name, inputs, outputs, and settings.

You can create the YAML file, or use the `@pipeline()` function to create the YAML file.

---
Review the [reference documentation for the `@pipeline()` function](https://learn.microsoft.com/en-us/python/api/azure-ai-ml/azure.ai.ml.dsl).

---
For example, if you want to build a pipeline that first prepares the data, and then trains the model, you can use the following code:

```python
from azure.ai.ml.dsl import pipeline

@pipeline()
def pipeline_function_name(pipeline_job_input):
    prep_data = loaded_component_prep(input_data=pipeline_job_input)
    train_model=loaded_component_train(training_data=prep_data.outputs.output_data)

    return {
        "pipeline_job_transformed_data": prep_data.outputs.output_data,
        "pipeline_job_trained_model": train_model.outputs.model_output,
    }
```

To pass a registered data asset as the pipeline job input, you can call the function you created with the data asset as input:
```python
from azure.ai.ml import Input
from azure.ai.ml.constants import AssetTypes

pipeline_job = pipeline_function_name(
    Input(type=AssetTypes.URI_FILE, 
    path="azureml:data:1"
))
```

The `@pipeline()` function builds a pipeline consisting of two sequential steps, represented by the two loaded components.

To understand the pipeline built in the example, let's explore it step by step:
````json
1. The pipeline is built by defining the function `pipeline_function_name`
2. The pipeline function expects `pipeline_job_input` as the overall pipeline input.
3. The first pipeline step requires a value for the input parameter `input_data`. The value for the input will be the value of `pipeline_job_input`.
4. The first pipeline step is defined by the loaded component for `prep_data`.
5. The value of the `output_data` of the first pipeline step is used for the expected input `training_data` of the second pipeline step.
6. The second pipeline step is defined by the loaded component for `train_model` and results in a trained model referred to by `model_output`.
7. Pipeline outputs are defined by returning variables from the pipeline function. There are two outputs:
    - `pipeline_job_transformed_data` with the value of `prep_data.outputs.output_data`
    - `pipeline_job_trained_model` with the value of `train_model.outputs.model_output`

````


![Diagram of pipeline structure including all inputs and outputs.](https://learn.microsoft.com/en-us/training/wwl-azure/run-pipelines-azure-machine-learning/media/pipeline-overview.png)

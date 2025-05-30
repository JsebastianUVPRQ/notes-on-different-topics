# Exam DP-100: ​Skills Measured

# Audience Profile

Candidates for the Azure Jo Associate certification should have subject matter expertise applying data science and machine learning to implement and run machine learning workloads on Azure.

Responsibilities for this role include planning and creating a suitable working environment for data science workloads on Azure. You run data experiments and train predictive models. In addition, you manage, optimize, and deploy machine learning models into production.

A candidate for this certification should have knowledge and experience in data science and using Azure Machine Learning and Azure Databricks.
# Perfil del público

Los candidatos a la certificación Azure Jo Associate deben tener experiencia en la materia aplicando la ciencia de datos y el aprendizaje automático para implementar y ejecutar cargas de trabajo de aprendizaje automático en Azure.

Las responsabilidades de este puesto incluyen la planificación y creación de un entorno de trabajo adecuado para las cargas de trabajo de ciencia de datos en Azure. Usted ejecuta experimentos de datos y entrena modelos predictivos. Además, usted gestiona, optimiza y despliega modelos de aprendizaje automático en producción.

El candidato a esta certificación debe tener conocimientos y experiencia en ciencia de datos y en el uso de Azure Machine Learning y Azure Databricks.

## Habilidades que se miden

NOTA: Las viñetas que aparecen debajo de cada una de las habilidades medidas pretenden ilustrar cómo estamos evaluando esa habilidad. Esta lista NO es definitiva ni exhaustiva. NOTA: La mayoría de las preguntas cubren características que están en Disponibilidad General (GA). El examen puede contener preguntas sobre características Preview si dichas características se utilizan habitualmente.

## Gestionar los recursos de Azure para el aprendizaje automático (25-30%)

### Crear un espacio de trabajo de Azure Machine Learning

- crear un espacio de trabajo de Azure Machine Learning
    
- configurar los ajustes del espacio de trabajo
    
- gestionar un espacio de trabajo utilizando Azure Machine Learning studio
    

### Gestionar los datos en un espacio de trabajo de Azure Machine Learning

- seleccionar los recursos de almacenamiento de Azure
    
- registrar y mantener almacenes de datos
    
- crear y gestionar conjuntos de datos
    

### Gestionar la computación para experimentos en Azure Machine Learning

- determinar las especificaciones informáticas adecuadas para una carga de trabajo de entrenamiento
    
- crear objetivos de cálculo para experimentos y formación
    
- configurar los recursos informáticos adjuntos, incluidos los Azure Databricks
    
- supervisar la utilización de la computación
    

### Implementar la seguridad y el control de acceso en Azure Machine Learning

- determinar los requisitos de acceso y asignar los requisitos a roles incorporados
    
- crear roles personalizados
    
- gestionar la pertenencia a roles
    
- gestionar credenciales utilizando Azure Key Vault
    

### Configurar un entorno de desarrollo de Azure Machine Learning

- crear instancias de cálculo
    
- compartir instancias de cálculo
    
- acceder a los espacios de trabajo de Azure Machine Learning desde otros entornos de desarrollo
    

### Configurar un espacio de trabajo Azure Databricks

- crear un espacio de trabajo Azure Databricks
    
- crear un clúster Azure Databricks
    
- crear y ejecutar cuadernos en Azure Databricks
    
- vincule un espacio de trabajo Azure Databricks a un espacio de trabajo Azure Machine Learning
    

## Ejecutar experimentos y entrenar modelos (20-25%)

### Cree modelos utilizando el diseñador de Azure Machine Learning

- cree un [[pipeline]] de entrenamiento utilizando el diseñador de Azure Machine Learning
    
- ingiera datos en un pipeline de diseñador
    
- utilice módulos del diseñador para definir el flujo de datos de un pipeline
    
- utilice módulos de código personalizados en el diseñador
    

### Ejecutar scripts de entrenamiento de modelos

- cree y ejecute un experimento utilizando el SDK de Azure Machine Learning
    
- configurar los ajustes de ejecución de un script
    
- consumir datos de un conjunto de datos en un experimento utilizando el SDK de Azure Machine Learning
    
- ejecutar un script de entrenamiento en el ordenador Azure Databricks
    
- ejecutar código para entrenar un modelo en un cuaderno Azure Databricks
    

### Genere métricas a partir de la ejecución de un experimento

- registrar métricas de la ejecución de un experimento
    
- recupere y visualice los resultados del experimento
    
- utilice los registros para solucionar errores de ejecución de experimentos
    
- utilizar MLflow para rastrear experimentos
    
- realizar un seguimiento de los experimentos que se ejecutan en Azure Databricks
    

### Utilice el aprendizaje automático automatizado para crear modelos óptimos

- utilice la interfaz de ML Automatizado en Azure Machine Learning studio
    
- utilice Automated ML desde el SDK de Azure Machine Learning
    
- seleccione las opciones de preprocesamiento
    
- seleccione los algoritmos a buscar
    
- defina una métrica principal
    
- obtener datos para una ejecución de Automated ML recuperar el mejor modelo
    

### Ajuste los hiperparámetros con Azure Machine Learning

- seleccionar un método de muestreo
    
- definir el espacio de búsqueda
    
- definir la métrica primaria
    
- defina las opciones de terminación anticipada
    
- encontrar el modelo que tenga valores óptimos de hiperparámetros
    

## Desplegar y hacer operativas las soluciones de aprendizaje automático (35-40%)

### Seleccionar la computación para el despliegue del modelo

- considere la seguridad de los servicios desplegados
    
- evalúe las opciones de computación para el despliegue
    

### Despliegue de un modelo como servicio

- configurar los ajustes de despliegue
    
- desplegar un modelo registrado
    
- desplegar un modelo entrenado en Azure Databricks en un [[endpoint]] de Azure Machine Learning
    
- consumir un servicio desplegado
    
- solucionar problemas del contenedor de despliegue
    

### Gestionar modelos en Azure Machine Learning

- registrar un modelo entrenado
    
- supervisar el uso del modelo
    
- supervisar la deriva de los datos
    

### Crear una [[Pipeline]] de Azure Machine Learning para la inferencia por lotes

- configurar un ParallelRunStep
    
- configurar el cálculo para una canalización de inferencia por lotes
    
- publicar una canalización de inferencia por lotes
    
- ejecutar una [[Pipeline]] de inferencia por lotes y obtener salidas
    
- obtener salidas de un ParallelRunStep
    

### Publicar una canalización de diseño de Azure Machine Learning como un servicio web

- crear un recurso informático de destino
    
- configurar una canalización de inferencia
    
- consumir un [[endpoint]] desplegado
    

### Implementar canalizaciones utilizando el SDK de Azure Machine Learning

- crear una canalización
    
- pasar datos entre los pasos de una canalización
    
- ejecutar una canalización
    
- monitorizar la ejecución de un pipeline
    

### Aplicar prácticas de ML Ops

- desencadenar un pipeline de Azure Machine Learning desde Azure DevOps
    
- automatizar el reentrenamiento de modelos basado en nuevas adiciones de datos o cambios en los datos
    
- refactorizar cuadernos en scripts
    
- implementar control de código fuente para scripts
    

## Implemente el aprendizaje automático responsable (5-10%)

### Utilizar explicadores de modelos para interpretar modelos

- seleccione un intérprete de modelos
    
- generar datos de importancia de características
    

### Describa las consideraciones de equidad de los modelos

- evaluar la equidad de los modelos en función de la disparidad de las predicciones
    
- mitigar la injusticia de los modelos
    

### Describir las consideraciones relativas a la privacidad de los datos

- describir los principios de la privacidad diferencial
    
- especificar los niveles aceptables de ruido en los datos y los efectos sobre la privacidad

## Skills Measured

NOTE: The bullets that appear below each of the skills measured are intended to illustrate how we are assessing that skill. This list is NOT definitive or exhaustive. NOTE: Most questions cover features that are General Availability (GA). The exam may contain questions on Preview features if those features are commonly used.

## Manage Azure resources for machine learning (25-30%)

### Create an Azure Machine Learning workspace

- create an Azure Machine Learning workspace
    
- configure workspace settings
    
- manage a workspace by using Azure Machine Learning studio
    

### Manage data in an Azure Machine Learning workspace

- select Azure storage resources
    
- register and maintain datastores
    
- create and manage datasets
    

### Manage compute for experiments in Azure Machine Learning

- determine the appropriate compute specifications for a training workload
    
- create compute targets for experiments and training
    
- configure Attached Compute resources including Azure Databricks
    
- monitor compute utilization
    

### Implement security and access control in Azure Machine Learning

- determine access requirements and map requirements to built-in roles
    
- create custom roles
    
- manage role membership
    
- manage credentials by using Azure Key Vault
    

### Set up an Azure Machine Learning development environment

- create compute instances
    
- share compute instances
    
- access Azure Machine Learning workspaces from other development environments
    

### Set up an Azure Databricks workspace

- create an Azure Databricks workspace
    
- create an Azure Databricks cluster
    
- create and run notebooks in Azure Databricks
    
- link and Azure Databricks workspace to an Azure Machine Learning workspace
    

## Run experiments and train models (20-25%)

### Create models by using the Azure Machine Learning designer

- create a training pipeline by using Azure Machine Learning designer
    
- ingest data in a designer pipeline
    
- use designer modules to define a pipeline data flow
    
- use custom code modules in designer
    

### Run model training scripts

- create and run an experiment by using the Azure Machine Learning SDK
    
- configure run settings for a script
    
- consume data from a dataset in an experiment by using the Azure Machine Learning SDK
    
- run a training script on Azure Databricks compute
    
- run code to train a model in an Azure Databricks notebook
    

### Generate metrics from an experiment run

- log metrics from an experiment run
    
- retrieve and view experiment outputs
    
- use logs to troubleshoot experiment run errors
    
- use MLflow to track experiments
    
- track experiments running in Azure Databricks
    

### Use Automated Machine Learning to create optimal models

- use the Automated ML interface in Azure Machine Learning studio
    
- use Automated ML from the Azure Machine Learning SDK
    
- select pre-processing options
    
- select the algorithms to be searched
    
- define a primary metric
    
- get data for an Automated ML run retrieve the best model
    

### Tune hyperparameters with Azure Machine Learning

- select a sampling method
    
- define the search space
    
- define the primary metric
    
- define early termination options
    
- find the model that has optimal hyperparameter values
    

## Deploy and operationalize machine learning solutions (35-40%)

### Select compute for model deployment

- consider security for deployed services
    
- evaluate compute options for deployment
    

### Deploy a model as a service

- configure deployment settings
    
- deploy a registered model
    
- deploy a model trained in Azure Databricks to an Azure Machine Learning [[endpoint]]
    
- consume a deployed service
    
- troubleshoot deployment container issues
    

### Manage models in Azure Machine Learning

- register a trained model
    
- monitor model usage
    
- monitor data drift
    

### Create an Azure Machine Learning pipeline for batch inferencing

- configure a ParallelRunStep
    
- configure compute for a batch inferencing pipeline
    
- publish a batch inferencing pipeline
    
- run a batch inferencing pipeline and obtain outputs
    
- obtain outputs from a ParallelRunStep
    

### Publish an Azure Machine Learning designer pipeline as a web service

- create a target compute resource
    
- configure an inference pipeline
    
- consume a deployed [[endpoint]]
    

### Implement pipelines by using the Azure Machine Learning SDK

- create a pipeline
    
- pass data between steps in a pipeline
    
- run a pipeline
    
- monitor pipeline runs
    

### Apply ML Ops practices

- trigger an Azure Machine Learning pipeline from Azure DevOps
    
- automate model retraining based on new data additions or data changes
    
- refactor notebooks into scripts
    
- implement source control for scripts
    

## Implement responsible machine learning (5-10%)

### Use model explainers to interpret models

- select a model interpreter
    
- generate feature importance data
    

### Describe fairness considerations for models

- evaluate model fairness based on prediction disparity
    
- mitigate model unfairness
    

### Describe privacy considerations for data

- describe principles of differential privacy
    
- specify acceptable levels of noise in data and the effects on privacy
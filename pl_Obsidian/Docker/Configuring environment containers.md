
Usually, environments for experiment script are created in containers. The following code configures a script-based experiment to host the **env** environment created previously in a container (this is the default unless you use a **DockerConfiguration** with a **use_docker** attribute of **False**, in which case the environment is created directly in the compute target)
```python

from azureml.core import Experiment, ScriptRunConfig

from azureml.core.runconfig import DockerConfiguration

  

docker_config = DockerConfiguration(use_docker=True)

  

script_config = ScriptRunConfig(source_directory='my_folder',

                                script='my_script.py',

                                environment=env,

                                docker_runtime_config=docker_config)
```
Azure Machine Learning utiliza una biblioteca de imágenes base para contenedores, eligiendo la base adecuada para el objetivo de cómputo que especifiques (por ejemplo, incluyendo soporte para Cuda en cómputo basado en GPU). Si has creado imágenes de contenedores personalizadas y las has registrado en un registro de contenedores, puedes sobrescribir las imágenes base predeterminadas y usar las tuyas propias modificando los atributos de la propiedad docker del entorno.

```python
from azureml.core import Environment

# Crear un nuevo entorno o cargar uno existente
env = Environment(name="my-environment")

# Configurar la imagen base de Docker y el registro de contenedores
env.docker.base_image = 'my-base-image'
env.docker.base_image_registry.address = 'myregistry.azurecr.io'
env.docker.base_image_registry.username = 'my-username'  # si es necesario
env.docker.base_image_registry.password = 'my-password'  # si es necesario

# Opcionalmente, registrar el entorno en el workspace
from azureml.core import Workspace
ws = Workspace.from_config()
env.register(workspace=ws)
```
## Environment

Una vez que has configurado y registrado el entorno, puedes utilizarlo en tus experimentos o despliegues. Aquí hay un ejemplo de cómo usar el entorno en una configuración de experimento:

```python
from azureml.core import ScriptRunConfig

# Configurar el experimento con el entorno
src = ScriptRunConfig(source_directory='.',
                      script='train.py',
                      compute_target='my-compute-cluster',
                      environment=env)

# Enviar el experimento
from azureml.core import Experiment
experiment = Experiment(workspace=ws, name='my-experiment')
run = experiment.submit(src)
run.wait_for_completion(show_output=True)

```

 
## Registering and reusing environments

After you've created an environment, you can register it in your workspace and reuse it for future experiments that have the same Python dependencies.
### Registering an environment

Use the **register** method of an **Environment** object to register an environment
```dockerfile

env.register(workspace=ws)
```
You can view the registered environments in your workspace like this:
```python
from azureml.core import Environment

env_names = Environment.list(workspace=ws)

for env_name in env_names:

    print('Name:',env_name)
```
## Retrieving and using an environment

You can retrieve a registered environment by using the **get** method of the ***Environment** class, and then assign it to a ***ScriptRunConfig***.

For example, the following code sample retrieves the ___training_environment___ registered environment, and assigns it to a script run configuration:
```python
from azureml.core import Environment, ScriptRunConfig

  

training_env = Environment.get(workspace=ws, name='training_environment')

  

script_config = ScriptRunConfig(source_directory='my_folder',

                                script='my_script.py',

                                environment=training_env)
```

When an experiment based on the estimator is run, Azure Machine Learning will look for an existing environment that matches the definition, and if none is found a new environment will be created based on the registered environment specification
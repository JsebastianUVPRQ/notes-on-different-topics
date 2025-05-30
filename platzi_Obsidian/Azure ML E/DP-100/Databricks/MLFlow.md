*Nota:*
---
La administración del ciclo de vida de ML en Databricks se proporciona mediante la administración de [MLflow](https://www.mlflow.org/). Azure Databricks proporciona una versión hospedada y totalmente administrada de MLflow integrada con características de seguridad empresarial, alta disponibilidad y otras características del área de trabajo de Azure Databricks, como la administración de experimentos y ejecuciones y la captura de revisiones de cuadernos. Los nuevos usuarios deberían empezar por el [Introducción a los experimentos de MLflow](https://learn.microsoft.com/es-es/azure/databricks/mlflow/quick-start-python), en el que se muestran las API básicas de seguimiento de MLflow.

---
MLflow es una plataforma de código abierto para administrar el ciclo de vida completo del aprendizaje automático. Tiene los siguientes componentes principales:

- Seguimiento: Permite realizar un seguimiento de los experimentos para registrar y comparar parámetros y resultados.
- Modelos: Permiten administrar e implementar modelos desde una variedad de bibliotecas de Machine Learning para una variedad de plataformas de inferencia y visualización de modelos.
- Proyectos: Permiten empaquetar el código de Machine Learning en una forma reutilizable y reproducible para compartirlo con otros científicos de datos o transferirlos a producción.
- Registro de modelos: Le permite centralizar un almacén de modelos para administrar las transiciones entre las etapas del ciclo de vida completo de los modelos, desde el almacenamiento provisional a producción, con funcionalidades que permiten crear versiones y anotaciones. Databricks proporciona una versión administrada del Registro de modelos en Unity Catalog.
- Servicio de modelos: Permite hospedar modelos de MLflow como puntos de conexión REST. Databricks proporciona una interfaz unificada para implementar, controlar y consultar los modelos de IA servidos.

MLflow admite [Java](https://www.mlflow.org/docs/latest/java_api/index.html), [Python](https://www.mlflow.org/docs/latest/python_api/index.html), [R](https://www.mlflow.org/docs/latest/R-api.html) y [API REST](https://docs.databricks.com/api/azure/workspace/experiments).

Azure Databricks cifra los datos de MLflow mediante una clave administrada por la plataforma. No se admite el cifrado mediante [claves administradas por el cliente para servicios administrados](https://learn.microsoft.com/es-es/azure/databricks/security/keys/cmk-managed-services-azure/).


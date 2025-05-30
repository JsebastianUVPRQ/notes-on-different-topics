Después de ingerir datos de los orígenes, puede usar la plataforma de Azure Databricks para explorar y analizar los datos de forma colaborativa.

Vamos a explorar las herramientas que se usan al trabajar con datos en Azure Databricks.

## Colaboración y ejecución de código con cuadernos

Puede usar **cuadernos** en Azure Databricks para escribir código de Python, SQL, Scala o R para explorar y visualizar datos. Los cuadernos admiten la exploración interactiva de datos y se pueden compartir entre los miembros del equipo. También admite funcionalidades de generación de perfiles de datos para que los científicos de datos comprendan la forma y el contenido de los datos.

[![Captura de pantalla de los idiomas disponibles en los cuadernos de Azure Databricks.](https://learn.microsoft.com/es-es/training/wwl-data-ai/perform-data-analysis-azure-databricks/media/azure-databricks-language.png)](https://learn.microsoft.com/es-es/training/wwl-data-ai/perform-data-analysis-azure-databricks/media/azure-databricks-language.png#lightbox)

Después de ingerir datos de los orígenes, puede usar la plataforma de Azure Databricks para explorar y analizar los datos [[Perform Data Science with Databricks]] de forma colaborativa.

Vamos a explorar las herramientas que se usan al trabajar con datos en Azure Databricks.

## Colaboración y ejecución de código con cuadernos

Puede usar **cuadernos** en Azure Databricks para escribir código de Python, SQL, Scala o R para explorar y visualizar datos. Los cuadernos admiten la exploración interactiva de datos y se pueden compartir entre los miembros del equipo. También admite funcionalidades de generación de perfiles de datos para que los científicos de datos comprendan la forma y el contenido de los datos.

[![Captura de pantalla de los idiomas disponibles en los cuadernos de Azure Databricks.](https://learn.microsoft.com/es-es/training/wwl-data-ai/perform-data-analysis-azure-databricks/media/azure-databricks-language.png)](https://learn.microsoft.com/es-es/training/wwl-data-ai/perform-data-analysis-azure-databricks/media/azure-databricks-language.png#lightbox)
Puede usar las **visualizaciones** integradas para comprender rápidamente las distribuciones de datos, las tendencias y los patrones. Junto a las características integradas, Azure Databricks le permite integrarse con bibliotecas de código abierto más usadas, como Matplotlib, Seaborn o D3.js para visualizaciones más complejas.

## Trabajar con DataFrames de Spark

Al trabajar con datos en cuadernos, se usa **DataFrames de Spark** que se basan en Apache Spark. Los DataFrames permiten manipular grandes conjuntos de datos de forma eficaz.

Para crear un DataFrame simple, puede ejecutar el código siguiente:
```python
data = [("Alice", 34), ("Bob", 45), ("Cathy", 29)] columns = ["Name", "Age"] df = spark.createDataFrame(data, columns)
```
DataFrames admite operaciones como el filtrado, la agregación y la unión, que son cruciales para la exploración de datos.

Por ejemplo, puede filtrar un DataFrame:
```python
filtered_df = df.filter(df["Age"] > 30)
```

## notebooks en databricks de SQL con python
Azure Databricks también admite **SQL** al permitir cambiar entre operaciones DataFrame y consultas SQL para interactuar con los datos de una manera que se sienta más natural.

Para filtrar el DataFrame mediante una consulta SQL, primero debe crear una vista temporal:
```python
df.createOrReplaceTempView("people") # Temporal view

sql_df = spark.sql("SELECT Name, Age FROM people WHERE Age > 30")
```


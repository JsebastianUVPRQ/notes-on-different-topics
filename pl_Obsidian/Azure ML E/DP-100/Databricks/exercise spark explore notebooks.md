## Ingest data

1. In the first cell of the notebook, enter the following code, which uses _shell_ commands to download data files from GitHub into the file system used by your cluster.
  
    ```python
     %sh
     rm -r /dbfs/spark_lab
     mkdir /dbfs/spark_lab
     wget -O /dbfs/spark_lab/2019.csv https://raw.githubusercontent.com/MicrosoftLearning/mslearn-databricks/main/data/2019.csv
     wget -O /dbfs/spark_lab/2020.csv https://raw.githubusercontent.com/MicrosoftLearning/mslearn-databricks/main/data/2020.csv
     wget -O /dbfs/spark_lab/2021.csv https://raw.githubusercontent.com/MicrosoftLearning/mslearn-databricks/main/data/2021.csv
    ```
    
2. Use the **▸ Run Cell** menu option at the left of the cell to run it. Then wait for the Spark job run by the code to complete.
    

## Query data in files

1. Move the mouse under the existing code cell, and use the **+ Code** icon that appears to add a new code cell. Then in the new cell, enter and run the following code to load the data from the files and view the first 100 rows.
    ```python
    df = spark.read.load('spark_lab/*.csv', format='csv')
    display(df.limit(100))
    ```
    
2. View the output and note that the data in the file relates to sales orders, but doesn’t include the column headers or information about the data types. To make more sense of the data, you can define a _schema_ for the dataframe.
    
3. Add a new code cell and use it to run the following code, which defines a schema for the data:
    ```python
    from pyspark.sql.types import *
    from pyspark.sql.functions import *
    orderSchema = StructType([
         StructField("SalesOrderNumber", StringType()),
         StructField("SalesOrderLineNumber", IntegerType()),
         StructField("OrderDate", DateType()),
         StructField("CustomerName", StringType()),
         StructField("Email", StringType()),
         StructField("Item", StringType()),
         StructField("Quantity", IntegerType()),
         StructField("UnitPrice", FloatType()),
         StructField("Tax", FloatType())
    ])
    df = spark.read.load('/spark_lab/*.csv', format='csv', schema=orderSchema)
    display(df.limit(100))
    ```
    
4. Observe that this time, the dataframe includes column headers. Then add a new code cell and use it to run the following code to display details of the dataframe schema, and verify that the correct data types have been applied:
    ```python
    df.printSchema()
    ```
## Query data using Spark SQL

1. Add a new code cell and use it to run the following code:

    ```python
    df.createOrReplaceTempView("salesorders")
    spark_df = spark.sql("SELECT * FROM salesorders")
    display(spark_df)
    ```

The native methods of the dataframe object you used previously enable you to query and analyze data quite effectively. However, many data analysts are more comfortable working with SQL syntax. Spark SQL is a SQL language API in Spark that you can use to run SQL statements, or even persist data in relational tables.

The code you just ran creates a relational _view_ of the data in a dataframe, and then uses the **spark.sql** library to embed Spark SQL syntax within your Python code and query the view and return the results as a dataframe.
## View results as a visualization

1. In a new code cell, run the following code to query the **salesorders** table:

    ```sql
    %sql
        
    SELECT * FROM salesorders
    ```

Above the table of results, select **+** and then select **Visualization** to view the visualization editor, and then apply the following options:
    - **Visualization type**: Bar
    - **X Column**: Item
    - **Y Column**: _Add a new column and select_ **Quantity**. _Apply the_ **Sum** _aggregation_.
3. Save the visualization and then re-run the code cell to view the resulting chart in the notebook.

## Get started with matplotlib

1. In a new code cell, run the following code to retrieve some sales order data into a dataframe:
    ```python
    sqlQuery = "SELECT CAST(YEAR(OrderDate) AS CHAR(4)) AS OrderYear, \
                    SUM((UnitPrice * Quantity) + Tax) AS GrossRevenue \
             FROM salesorders \
             GROUP BY CAST(YEAR(OrderDate) AS CHAR(4)) \
             ORDER BY OrderYear"
    df_spark = spark.sql(sqlQuery)
    df_spark.show()
    ```
    
2. Add a new code cell and use it to run the following code, which imports the **matplotlib** and uses it to create a chart:

    ```python
    from matplotlib import pyplot as plt
        
    # matplotlib requires a Pandas dataframe, not a Spark one
    df_sales = df_spark.toPandas()
    # Create a bar plot of revenue by year
    plt.bar(x=df_sales['OrderYear'], height=df_sales['GrossRevenue'])
    # Display the plot
    plt.show()
    ```
    
3. Review the results, which consist of a column chart with the total gross revenue for each year. Note the following features of the code used to produce this chart:
    - The **matplotlib** library requires a Pandas dataframe, so you need to convert the Spark dataframe returned by the Spark SQL query to this format.
    - At the core of the **matplotlib** library is the **pyplot** object. This is the foundation for most plotting functionality.
4. The default settings result in a usable chart, but there’s considerable scope to customize it. Add a new code cell with the following code and run it:

    ```python
    # Clear the plot area
    plt.clf()
    # Create a bar plot of revenue by year
    plt.bar(x=df_sales['OrderYear'], height=df_sales['GrossRevenue'], color='orange')
    # Customize the chart
    plt.title('Revenue by Year')
    plt.xlabel('Year')
    plt.ylabel('Revenue')
    plt.grid(color='#95a5a6', linestyle='--', linewidth=2, axis='y', alpha=0.7)
    plt.xticks(rotation=45)
    # Show the figure
    plt.show()
    ```
    
1. A plot is technically contained with a **Figure**. In the previous examples, the figure was created implicitly for you; but you can create it explicitly. Try running the following in a new cell:
    ```python
    # Clear the plot area
    plt.clf()
    # Create a Figure
    fig = plt.figure(figsize=(8,3))
    # Create a bar plot of revenue by year
    plt.bar(x=df_sales['OrderYear'], height=df_sales['GrossRevenue'], color='orange')
    # Customize the chart
    plt.title('Revenue by Year')
    plt.xlabel('Year')
    plt.ylabel('Revenue')
    plt.grid(color='#95a5a6', linestyle='--', linewidth=2, axis='y', alpha=0.7)
    plt.xticks(rotation=45)
    # Show the figure
    plt.show()
    ```
    
2. A figure can contain multiple subplots, each on its own axis. Use this code to create multiple charts:
   
    ```python
    # Clear the plot area
    plt.clf()
    # Create a figure for 2 subplots (1 row, 2 columns)
    fig, ax = plt.subplots(1, 2, figsize = (10,4))
    # Create a bar plot of revenue by year on the first axis
    ax[0].bar(x=df_sales['OrderYear'], height=df_sales['GrossRevenue'], color='orange')
    ax[0].set_title('Revenue by Year')
    # Create a pie chart of yearly order counts on the second axis
    yearly_counts = df_sales['OrderYear'].value_counts()
    ax[1].pie(yearly_counts)
    ax[1].set_title('Orders per Year')
    ax[1].legend(yearly_counts.keys().tolist())
    # Add a title to the Figure
    fig.suptitle('Sales Data')
    # Show the figure
    plt.show()
    ```

## Use the seaborn library

1. Add a new code cell and use it to run the following code, which uses the **seaborn** library (which is built on matplotlib and abstracts some of its complexity) to create a chart:
    
    codeCopy
    
    ```python
    import seaborn as sns
       
    # Clear the plot area
    plt.clf()
    # Create a bar chart
    ax = sns.barplot(x="OrderYear", y="GrossRevenue", data=df_sales)
    plt.show()
    ```
    
2. The **seaborn** library makes it simpler to create complex plots of statistical data, and enables you to control the visual theme for consistent data visualizations. Run the following code in a new cell:
    
    codeCopy
    
    ```python
    # Clear the plot area
    plt.clf()
       
    # Set the visual theme for seaborn
    sns.set_theme(style="whitegrid")
       
    # Create a bar chart
    ax = sns.barplot(x="OrderYear", y="GrossRevenue", data=df_sales)
    plt.show()
    ```
    
3. Like matplotlib. seaborn supports multiple chart types. Run the following code to create a line chart:
    
    codeCopy
    
    ```python
    # Clear the plot area
    plt.clf()
       
    # Create a bar chart
    ax = sns.lineplot(x="OrderYear", y="GrossRevenue", data=df_sales)
    plt.show()
    ```
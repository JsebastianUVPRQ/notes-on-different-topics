El algoritmo K-means funciona de la forma siguiente:

1. Inicializa las coordenadas _K_ como puntos seleccionados aleatoriamente denominados _centroides_ en un espacio dimensional _n_ (donde _n_ es el número de dimensiones de los vectores de características).
2. Traza los vectores de las características como puntos en el mismo espacio y asigna cada punto a su centroide más cercano.
3. Mueve los centroides al centro de los puntos que tiene asignados, en función de la distancia _media_.
4. Reasigna los puntos a su centroide más cercano después del movimiento.
5. Repite los pasos 3 y 4 hasta que las asignaciones de clústeres se estabilizan o hasta que se completa el número de iteraciones especificado.


When the experiment run has finished, select the **Evaluate Model** module and in the settings pane, on the **Outputs + Logs** tab, under **Data outputs** in the **Evaluation results** section, use the **Visualize** icon to view the performance metrics. These metrics can help data scientists assess how well the model separates the clusters. They include a row of metrics for each cluster, and a summary row for a combined evaluation. The metrics in each row are: 

- **Average Distance to Other Center**: This indicates how close, on average, each point in the cluster is to the centroids of all other clusters. 
    
- **Average Distance to Cluster Center**: This indicates how close, on average, each point in the cluster is to the centroid of the cluster. 
    
- **Number of Points**: The number of points assigned to the cluster. 
    
- **Maximal Distance to Cluster Center**: The maximum of the distances between each point and the centroid of that point’s cluster. If this number is high, the cluster may be widely dispersed. This statistic in combination with the **Average Distance to Cluster Center** helps you determine the cluster’s _spread_.
Veamos los datos básicos que nos brinda pandas: Cantidad y nombre de columnas 
```Python
print('Cantidad de Filas y columnas:',df.shape) 
print('Nombre columnas:',df.columns)

#Columnas, nulos y tipos de datos:
df.info()

# Descripción estadística de los datos numéricos:
df.describe() #Pandas filtra las features numéricas y calcula datos estadísticos que pueden ser útiles: cantidad, media, desvío estándar, valores máximo y mínimo.

#Verificar si hay correlación entre los datos:
corr = df.set_index('alpha_3').corr()
sm.graphics.plot_corr(corr, xnames=list(corr.columns)) 
plt.show()
```
![[Pasted image 20230821004626.png]]
En este caso vemos baja correlación entre las variables. Dependiendo del algoritmo que utilicemos podría ser una buena decisión eliminar features que tuvieran alta correlación. Cargamos un segundo archivo csv para ahondar en el crecimiento de la población en los últimos años, filtramos a España y visualizamos.

```Python
url = 'https://raw.githubusercontent.com/DrueStaples/Population_Growth/master/countr\ies.csv' 
df_pop = pd.read_csv(url)
print(df_pop.head(5)) 
df_pop_es = df_pop[df_pop["country"] == 'Spain' ]
print(df_pop_es.head())
df_pop_es.drop(['country'],axis=1)['population'].plot(kind='bar')
#--------------------------------------------------------------------------------
#Hagamos la comparativa con otro país, por ejemplo con el crecimiento poblacional en Argentina
df_pop_ar = df_pop[(df_pop["country"] == 'Argentina')]
anios = df_pop_es['year'].unique()
pop_ar = df_pop_ar['population'].values
pop_es = df_pop_es['population'].values

df_plot = pd.DataFrame({'Argentina': pop_ar, 'Spain': pop_es},
					   index=anios)
df_plot.plot(kind='bar')
```
![[Pasted image 20230821005141.png]]
```Python
#Ahora filtremos todos los paises hispano-hablantes.
df_espanol = df.replace(np.nan, '', regex=True)
df_espanol = df_espanol[ df_espanol['languages'].str.contains('es') ]
df_espanol
#Además, la visualización
df_espanol.set_index('alpha_3')[['population','area']].plot(kind='bar',rot=65,figsize=(20,10))```
![[Pasted image 20230821005417.png]]
![[Pasted image 20230821005451.png]]
Vamos a hacer detección de Outliers²³, en este caso definimos como límite superior (e inferior) la media más (menos) “2 veces la "Desviacion estandar"” que muchas veces es tomada como máximos de tolerancia.
```Python
1 anomalies = []
2
3 # Funcion ejemplo para detección de outliers
4 def find_anomalies(data):
5 # Set upper and lower limit to 2 standard deviation
6 data_std = data.std()
7 data_mean = data.mean()
8 anomaly_cut_off = data_std * 2
9 lower_limit = data_mean - anomaly_cut_off
10 upper_limit = data_mean + anomaly_cut_off
11 print(lower_limit.iloc[0])
12 print(upper_limit.iloc[0])
13
14 # Generate outliers
15 for index, row in data.iterrows():
16 outlier = row # # obtener primer columna
17 if (outlier.iloc[0] > upper_limit.iloc[0]) or (outlier.iloc[0] < lower_limit\
18 .iloc[0]):
19 anomalies.append(index)
20 return anomalies
21
22 find_anomalies(df_espanol.set_index('alpha_3')[['population']])
#-------------------------------------------
# Detectamos como outliers a Brasil y a USA. Los eliminamos y graficamos ordenado por población de menor a mayor.
#-------------------------------------------
1 # Quitemos BRA y USA por ser outliers y volvamos a graficar:
2 df_espanol.drop([30,233], inplace=True)
3 df_espanol.set_index('alpha_3')[['population','area']].sort_values(["population"]).p\
4 lot(kind='bar',rot=65,figsize=(20,10))
```
# Otros procesos comunes en EDA
tras pruebas y gráficas que se suelen hacer son:
• Si hay datos categóricos, agruparlos, contabilizarlos y ver su relación con las clases de salida.
• Gráficas de distribución en el tiempo, por ejemplo si tuviéramos ventas, para tener una primera
impresión sobre su estacionalidad.
• Rankings del tipo “10 productos más vendidos” o “10 ítems con más referencias por usuario”.
• Calcular importancia de Features y descartar las menos útiles.
NOTEBOOK DE CASOS MÁS ÚTILES: [GitHub][https://github.com/jbagnato/machine-learning/blob/master/Manipulacion_datos_pandas.ipynb]
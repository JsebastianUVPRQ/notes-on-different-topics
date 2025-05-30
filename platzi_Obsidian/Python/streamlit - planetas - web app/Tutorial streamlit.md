¡Claro! Aquí tienes un tutorial completo y a profundidad sobre cómo crear aplicaciones web con Streamlit en Python.

Streamlit es un framework open-source que permite a los desarrolladores de Python crear y compartir aplicaciones web interactivas y visuales para proyectos de ciencia de datos y machine learning con muy poco esfuerzo y sin necesidad de experiencia en desarrollo web frontend (HTML, CSS, JavaScript).

---

**Tutorial Completo de Streamlit**

**Índice:**

1. **Introducción a Streamlit:** ¿Qué es y por qué usarlo?
2. **Prerrequisitos:** Lo que necesitas antes de empezar.
3. **Instalación:** Cómo instalar Streamlit.
4. **Tu Primera Aplicación Streamlit:** "Hola Mundo".
5. **Comandos Esenciales de Streamlit:** Ejecución y estructura básica.
6. **Elementos de Texto y Datos:** Mostrar información.
7. **Widgets Interactivos:** Entrada del usuario.
8. **Layout y Organización:** Estructurando tu app (sidebar, columnas).
9. **Mostrar Multimedia:** Imágenes, Audio y Video.
10. **Gráficos y Visualizaciones:** Integración con librerías populares.
11. **Manejo de Estado (`st.session_state`):** Mantener información entre interacciones.
12. **Caché (`st.cache_data`, `st.cache_resource`):** Optimizar el rendimiento.
13. **Progreso y Estado:** Indicadores visuales.
14. **Ejemplo Práctico:** Una app un poco más compleja.
15. **Despliegue (Deployment):** Cómo compartir tu aplicación.
16. **Buenas Prácticas y Consejos.**
17. **Recursos Adicionales.**

---

**1. Introducción a Streamlit**

- **¿Qué es?** Un framework Python para construir rápidamente UIs para datos.
- **¿Por qué usarlo?**
    - **Simple y Rápido:** Escribe scripts de Python y Streamlit los convierte en una app web.
    - **Centrado en Python:** No necesitas saber HTML, CSS o JavaScript.
    - **Interactivo:** Widgets fáciles de usar para la entrada del usuario.
    - **Actualización Automática:** La app se actualiza automáticamente cuando guardas el script o interactúas con un widget.
    - **Ideal para:** Dashboards, visualización de datos, prototipos de modelos de ML, herramientas internas.

---

**2. Prerrequisitos**

- **Python:** Necesitas tener Python instalado (versión 3.7 o superior recomendada). Puedes descargarlo desde [python.org](https://www.python.org/).
- **Pip:** El gestor de paquetes de Python, usualmente viene incluido con Python.
- **(Recomendado) Entorno Virtual:** Es una buena práctica crear un entorno virtual para aislar las dependencias de tu proyecto.
    
    Bash
    
    ```
    # Crear un entorno virtual (ej. llamado .venv)
    python -m venv .venv
    # Activar el entorno (Windows)
    .\.venv\Scripts\activate
    # Activar el entorno (macOS/Linux)
    source .venv/bin/activate
    ```
    

---

**3. Instalación**

Abre tu terminal o línea de comandos (con tu entorno virtual activado si usas uno) y ejecuta:

Bash

```
pip install streamlit pandas numpy matplotlib plotly seaborn
```

- `streamlit`: El propio framework.
- `pandas`, `numpy`: Librerías esenciales para manipulación de datos (muy comunes en apps Streamlit).
- `matplotlib`, `plotly`, `seaborn`: Librerías populares para gráficos (opcionales, pero útiles).

---

**4. Tu Primera Aplicación Streamlit**

1. Crea un archivo Python, por ejemplo, `mi_primera_app.py`.
    
2. Escribe el siguiente código:
    
    Python
    
    ```python
    # mi_primera_app.py
    import streamlit as st
    import pandas as pd
    import numpy as np
    
    # Título de la aplicación
    st.title('Mi Primera Aplicación Streamlit :rocket:')
    
    # Texto simple
    st.write("¡Hola Mundo desde Streamlit!")
    
    # Usando Markdown para formato
    st.markdown("""
    Esta es una aplicación de ejemplo que muestra algunas
    funcionalidades básicas de **Streamlit**.
    
    * Podemos usar listas.
    * Y **formato** como *negrita* o *cursiva*.
    """)
    
    # Mostrar un DataFrame de Pandas
    st.header("Datos de Ejemplo")
    df = pd.DataFrame({
        'Columna A': [1, 2, 3, 4],
        'Columna B': [10, 20, 30, 40]
    })
    st.dataframe(df)
    
    # Mostrar un gráfico simple
    st.header("Gráfico Simple")
    chart_data = pd.DataFrame(
        np.random.randn(20, 3),
        columns=['a', 'b', 'c'])
    st.line_chart(chart_data)
    
    st.success("¡Aplicación cargada exitosamente!")
    ```
    

---

**5. Comandos Esenciales de Streamlit**

- Ejecutar la aplicación:
    
    Abre tu terminal en el directorio donde guardaste mi_primera_app.py y ejecuta:
    
    ```powershell
    streamlit run mi_primera_app.py
    ```
    
    Streamlit iniciará un servidor local y abrirá automáticamente la aplicación en tu navegador web. Verás la salida en la terminal, incluyendo la URL local (usualmente `http://localhost:8501`).
    
- **Flujo de Ejecución:**
    
    - Cada vez que guardas el archivo `.py` o interactúas con un widget, Streamlit **vuelve a ejecutar todo el script** de arriba a abajo.
    - Esto hace que el desarrollo sea muy rápido e intuitivo, pero es crucial entenderlo para manejar el estado y la optimización (ver secciones 11 y 12).

---

**6. Elementos de Texto y Datos**

Streamlit ofrece funciones para mostrar texto y datos de diversas formas:



```Python
import streamlit as st
import pandas as pd

# --- Texto ---
st.title("Título Principal")
st.header("Encabezado")
st.subheader("Sub-encabezado")
st.caption("Texto pequeño o pie de foto")

st.write("Texto general, puede mostrar casi cualquier cosa (strings, dataframes, etc.)")

st.markdown("Texto con formato **Markdown**: *cursiva*, `código`, [links](https://streamlit.io).")

st.code("""
# Bloque de código Python
def funcion_ejemplo():
    return "Hola"
""", language='python')

st.latex(r'''
a + ar + a r^2 + a r^3 + \cdots + a r^{n-1} =
\sum_{k=0}^{n-1} ar^k =
a \left(\frac{1-r^{n}}{1-r}\right)
''') # Muestra fórmulas LaTeX

# --- Datos ---
df = pd.DataFrame({'col1': [1, 2, 3], 'col2': [10, 20, 30]})

st.dataframe(df) # DataFrame interactivo (ordenar, buscar)
st.table(df)     # Tabla estática

st.metric(label="Temperatura", value="25 °C", delta="1.5 °C") # Métrica con indicador de cambio
st.metric(label="Ventas", value="1,200", delta="-8%", delta_color="inverse")

data_dict = {"nombre": "Ana", "edad": 30, "ciudad": "Madrid"}
st.json(data_dict) # Muestra un diccionario o JSON
```

---

**7. Widgets Interactivos**

Los widgets permiten a los usuarios interactuar con la aplicación. El valor del widget se devuelve como una variable en Python.

```Python
import streamlit as st
from datetime import time, date

st.header("Widgets Comunes")

# --- Botón ---
# Devuelve True si se hace clic en esta ejecución
if st.button('Haz clic aquí'):
    st.write('¡Botón presionado!')
else:
    st.write('Esperando clic...')

# --- Checkbox ---
# Devuelve True si está marcado
if st.checkbox('Mostrar información adicional'):
    st.write('Aquí tienes la información adicional.')

# --- Radio Buttons ---
# Devuelve la opción seleccionada
opcion_radio = st.radio(
    "Elige tu opción favorita:",
    ('Opción A', 'Opción B', 'Opción C'))
st.write(f'Seleccionaste: {opcion_radio}')

# --- Selectbox (Dropdown) ---
# Devuelve la opción seleccionada
opcion_select = st.selectbox(
    'Elige un color:',
    ['Rojo', 'Verde', 'Azul'])
st.write(f'Color elegido: {opcion_select}')

# --- Multiselect ---
# Devuelve una lista con las opciones seleccionadas
opciones_multi = st.multiselect(
    'Elige tus frutas favoritas:',
    ['Manzana', 'Banana', 'Naranja', 'Pera'],
    default=['Manzana', 'Naranja']) # Opciones por defecto
st.write(f'Frutas seleccionadas: {opciones_multi}')

# --- Slider ---
# Devuelve el valor seleccionado
valor_slider = st.slider(
    'Selecciona un rango de valores',
    min_value=0.0, max_value=100.0, value=(25.0, 75.0)) # value puede ser un solo número o una tupla para rango
st.write(f'Rango seleccionado: {valor_slider}')

# --- Input de Texto ---
# Devuelve el texto introducido
nombre_usuario = st.text_input('Introduce tu nombre', 'Escribe aquí...')
if nombre_usuario != 'Escribe aquí...':
    st.write(f'Hola, {nombre_usuario}')

# --- Input Numérico ---
# Devuelve el número introducido
edad = st.number_input('Introduce tu edad', min_value=0, max_value=120, value=30, step=1)
st.write(f'Edad: {edad}')

# --- Área de Texto ---
texto_largo = st.text_area('Escribe un comentario', 'Deja tu feedback...')
st.write(f'Comentario: {texto_largo[:50]}...') # Muestra los primeros 50 caracteres

# --- Input de Fecha ---
fecha = st.date_input("Selecciona una fecha", date.today())
st.write(f'Fecha seleccionada: {fecha}')

# --- Input de Hora ---
hora = st.time_input("Selecciona una hora", time(8, 45))
st.write(f'Hora seleccionada: {hora}')

# --- Carga de Archivos ---
# Devuelve un objeto BytesIO o None
archivo_cargado = st.file_uploader("Carga un archivo CSV", type=["csv"])
if archivo_cargado is not None:
    # Para leer un CSV, por ejemplo:
    # import pandas as pd
    # dataframe = pd.read_csv(archivo_cargado)
    st.write("Archivo cargado:", archivo_cargado.name)
    st.success("Archivo procesado (simulado)")
```

---

**8. Layout y Organización**

Puedes estructurar tu aplicación usando la barra lateral (sidebar) y columnas.

```Python
import streamlit as st
import numpy as np

# --- Barra Lateral (Sidebar) ---
# Los elementos añadidos con st.sidebar. se mostrarán en la barra lateral izquierda
st.sidebar.header("Controles")
opcion_sidebar = st.sidebar.selectbox("Elige algo en la sidebar", ["A", "B"])
valor_slider_sidebar = st.sidebar.slider("Slider en la sidebar", 0, 10, 5)

st.header("Layout de la Aplicación")
st.write("Contenido Principal")
st.write(f"Opción de la Sidebar: {opcion_sidebar}")
st.write(f"Valor del Slider en Sidebar: {valor_slider_sidebar}")

# --- Columnas ---
# Crea columnas para poner elementos lado a lado
col1, col2, col3 = st.columns(3) # Puedes pasar un número o una lista de anchos [2, 1, 1]

with col1:
   st.subheader("Columna 1")
   st.write("Contenido de la primera columna.")
   if st.button("Botón en Col 1"):
       st.write("Clic en Col 1")

with col2:
   st.subheader("Columna 2")
   st.line_chart(np.random.randn(10, 1))

with col3:
   st.subheader("Columna 3")
   st.metric("Valor", 100, 5)

# --- Expander ---
# Sección colapsable
with st.expander("Haz clic para ver más detalles"):
    st.write("""
        Aquí puedes poner contenido detallado que no es esencial
        ver a primera vista. Ideal para explicaciones largas,
        configuraciones avanzadas, etc.
    """)

# --- Container ---
# Un contenedor para agrupar elementos visualmente o lógicamente
with st.container():
   st.write("Esto está dentro de un contenedor.")
   st.bar_chart(np.random.randn(50, 3))

st.write("Esto está fuera del contenedor.")

# --- Pestañas (Tabs) --- (Introducido en versiones más recientes)
tab1, tab2 = st.tabs(["Gráfico", "Datos"])

with tab1:
   st.header("Un gráfico")
   st.line_chart(np.random.randn(20, 2))

with tab2:
   st.header("Los datos")
   st.dataframe(np.random.randn(20, 2))
```

---

**9. Mostrar Multimedia**

```Python
import streamlit as st
from PIL import Image # Para manejo básico de imágenes

st.header("Multimedia")

# --- Imágenes ---
# Desde un archivo local o URL
# image = Image.open('ruta/a/tu/imagen.jpg') # Si es local
# st.image(image, caption='Una bonita imagen local', use_column_width=True)

# Desde una URL
st.image("https://static.streamlit.io/examples/owl.jpg",
         caption='Búho desde URL', width=300)

# --- Audio ---
# Desde archivo local o URL
# audio_file = open('ruta/a/tu/audio.ogg', 'rb')
# audio_bytes = audio_file.read()
# st.audio(audio_bytes, format='audio/ogg')

# Desde URL (ejemplo simulado, necesitas una URL real de audio)
# st.audio("URL_A_TU_ARCHIVO_DE_AUDIO.mp3")
st.caption("Ejemplo de Audio (necesitas un archivo o URL)")

# --- Video ---
# Desde archivo local o URL
# video_file = open('ruta/a/tu/video.mp4', 'rb')
# video_bytes = video_file.read()
# st.video(video_bytes)

# Desde URL (ej. YouTube)
st.video("https://www.youtube.com/watch?v=JwSS70SZdyM")
```

---

**10. Gráficos y Visualizaciones**

Streamlit se integra perfectamente con las librerías de gráficos más populares. También tiene algunos gráficos nativos simples.

```Python
import streamlit as st
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import plotly.express as px
import seaborn as sns

st.header("Gráficos y Visualizaciones")

# Datos de ejemplo
data = pd.DataFrame(
    np.random.randn(100, 3),
    columns=['a', 'b', 'c']
)

# --- Gráficos Nativos de Streamlit ---
st.subheader("Gráficos Nativos")
st.line_chart(data)
st.area_chart(data)
st.bar_chart(data['a'])
st.scatter_chart(data, x='a', y='b', color='c') # Nuevo gráfico de dispersión nativo

# --- Matplotlib ---
st.subheader("Matplotlib")
fig, ax = plt.subplots() # Crea una figura y ejes de Matplotlib
ax.scatter(data['a'], data['b'])
ax.set_title("Gráfico de Dispersión (Matplotlib)")
ax.set_xlabel("Columna A")
ax.set_ylabel("Columna B")
st.pyplot(fig) # Muestra la figura en Streamlit

# --- Seaborn (basado en Matplotlib) ---
st.subheader("Seaborn")
fig_sns = plt.figure() # Necesario crear una figura explícitamente a veces con Seaborn
sns.histplot(data['a'], kde=True)
plt.title("Histograma (Seaborn)")
st.pyplot(fig_sns)

# --- Plotly ---
st.subheader("Plotly")
fig_plotly = px.scatter(data, x='a', y='b', title="Gráfico de Dispersión Interactivo (Plotly)")
st.plotly_chart(fig_plotly, use_container_width=True) # use_container_width ajusta al ancho

# --- Altair --- (Necesitarías instalar altair: pip install altair vega_datasets)
# import altair as alt
# st.subheader("Altair")
# chart = alt.Chart(data).mark_circle().encode(
#     x='a', y='b', tooltip=['a', 'b', 'c']
# ).interactive()
# st.altair_chart(chart, use_container_width=True)

# --- Mapas ---
st.subheader("Mapas")
map_data = pd.DataFrame(
    np.random.randn(100, 2) / [50, 50] + [37.76, -122.4], # Coordenadas cerca de SF
    columns=['lat', 'lon'])
st.map(map_data)
```

---

**11. Manejo de Estado (`st.session_state`)**

Dado que Streamlit re-ejecuta el script completo en cada interacción, cualquier variable local se perderá. `st.session_state` es un objeto similar a un diccionario que persiste entre ejecuciones dentro de una misma sesión de usuario.

```Python
import streamlit as st

st.title("Contador con Estado de Sesión")

# Inicializar el contador en el estado de sesión si no existe
if 'count' not in st.session_state:
    st.session_state.count = 0

# Botones para incrementar y decrementar
col1, col2 = st.columns(2)
with col1:
    if st.button('Incrementar'):
        st.session_state.count += 1
with col2:
    if st.button('Decrementar'):
        st.session_state.count -= 1

# Mostrar el valor actual del contador
st.write('Contador:', st.session_state.count)

# También puedes acceder y modificar usando notación de atributos:
# st.session_state.mi_variable = "valor"
# print(st.session_state.mi_variable)
```

**Usos comunes de `st.session_state`:**

- Recordar valores de widgets entre interacciones.
- Almacenar resultados de cálculos que no necesitan caché pero deben persistir.
- Controlar flujos complejos (ej. pasos de un formulario).

---

**12. Caché (`st.cache_data`, `st.cache_resource`)**

Para evitar re-ejecutar cálculos costosos (cargar datos grandes, entrenar modelos) en cada interacción, Streamlit ofrece decoradores de caché.

- `@st.cache_data`: Ideal para _datos_ serializables (DataFrames, listas, dicts, resultados de cálculos). Streamlit hashea los argumentos de la función y el bytecode de la función. Si cambian, vuelve a ejecutar. Si no, devuelve el resultado cacheado.
    
- `@st.cache_resource`: Ideal para _recursos_ no serializables (conexiones a bases de datos, modelos de ML pesados). Streamlit solo ejecuta la función una vez y reutiliza el objeto devuelto en ejecuciones posteriores. **No** verifica cambios en los argumentos o el código de la función después de la primera ejecución.
    

```Python
import streamlit as st
import pandas as pd
import time
import requests # Para ejemplo de recurso

# --- @st.cache_data ---
# Cachea la carga y procesamiento de datos
@st.cache_data
def cargar_datos_pesados(url):
    print("Ejecutando cargar_datos_pesados...") # Se imprime solo la primera vez (o si url cambia)
    time.sleep(3) # Simula una carga lenta
    df = pd.read_csv(url)
    # Simulamos un procesamiento
    df['nueva_columna'] = df.iloc[:, 0] * 2
    return df

st.header("Demostración de Caché")
data_url = "https://raw.githubusercontent.com/plotly/datasets/master/gapminder_unfiltered.csv" # URL de ejemplo
st.write("Cargando datos (puede tardar la primera vez)...")
df_cargado = cargar_datos_pesados(data_url)
st.dataframe(df_cargado.head())
st.success("Datos cargados y cacheados.")

# Botón para forzar re-ejecución sin cambiar nada más
if st.button("Re-ejecutar script"):
    st.write("Script re-ejecutado, pero la función cacheada no se llamó de nuevo.")


# --- @st.cache_resource ---
# Cachea la creación de un recurso (ej. un modelo o conexión)
@st.cache_resource
def obtener_recurso_costoso():
    print("Ejecutando obtener_recurso_costoso...") # Se imprime solo una vez por sesión
    time.sleep(2) # Simula creación costosa
    # Imagina que esto es una conexión a BD o un modelo de ML cargado
    # return some_complex_object_or_connection
    return {"config": "valor_importante", "session_id": requests.Session()} # Ejemplo con objeto no simple

st.subheader("Caché de Recursos")
recurso = obtener_recurso_costoso()
st.write("Recurso obtenido (o reutilizado desde caché).")
st.write(f"ID de sesión del recurso: {id(recurso['session_id'])}") # El ID será el mismo en re-ejecuciones

if st.button("Re-ejecutar script (Recurso)"):
    st.write("Script re-ejecutado, pero la función de recurso no se llamó de nuevo.")

# Para limpiar el caché manualmente (útil durante el desarrollo):
# Clic en el menú (hamburguesa) de la app -> Clear cache
```

---

**13. Progreso y Estado**

Informa al usuario sobre operaciones largas.

Python

```
import streamlit as st
import time

st.header("Progreso y Estado")

# --- Barra de Progreso ---
if st.button("Iniciar tarea larga (progreso)"):
    st.write("Iniciando...")
    barra_progreso = st.progress(0)
    for porcentaje_completado in range(100):
        time.sleep(0.05) # Simula trabajo
        # Actualiza la barra de progreso
        barra_progreso.progress(porcentaje_completado + 1)
    st.success("¡Tarea completada!")

# --- Spinner ---
# Muestra un mensaje mientras se ejecuta un bloque de código
if st.button("Iniciar tarea con spinner"):
    with st.spinner('Esperando por favor...'):
        time.sleep(3) # Simula trabajo
    st.success('¡Hecho!')

# --- Mensajes de Estado ---
st.success("Mensaje de éxito.")
st.info("Mensaje informativo.")
st.warning("Mensaje de advertencia.")
st.error("Mensaje de error.")

# --- Excepciones ---
# Muestra excepciones de Python de forma amigable
try:
    resultado = 10 / 0
except ZeroDivisionError as e:
    st.exception(e)
```

---

**14. Ejemplo Práctico: Analizador Simple de Datos CSV**

Esta aplicación permitirá al usuario cargar un archivo CSV, seleccionar columnas y mostrar estadísticas básicas y un gráfico.

Python

```
# analizador_csv.py
import streamlit as st
import pandas as pd
import numpy as np
import plotly.express as px

st.set_page_config(layout="wide") # Usar layout ancho

st.title("📊 Analizador Simple de Archivos CSV")

# --- Carga del Archivo ---
uploaded_file = st.file_uploader("Carga tu archivo CSV", type=["csv"])

# Usar session state para guardar el dataframe y evitar recargas innecesarias
if 'df' not in st.session_state:
    st.session_state.df = None

if uploaded_file is not None:
    # Solo lee el archivo si no está ya cargado o si se carga uno nuevo
    if st.session_state.df is None or st.session_state.get('last_uploaded_filename') != uploaded_file.name:
        try:
            with st.spinner("Cargando datos..."):
                st.session_state.df = pd.read_csv(uploaded_file)
                st.session_state.last_uploaded_filename = uploaded_file.name
                st.success("Archivo cargado exitosamente!")
        except Exception as e:
            st.error(f"Error al leer el archivo CSV: {e}")
            st.session_state.df = None # Resetea si hay error
else:
    # Si no hay archivo cargado, resetea el estado
    if st.button("Limpiar estado (si hubo error previo)"):
         st.session_state.df = None
         st.session_state.pop('last_uploaded_filename', None) # Elimina el nombre del archivo guardado
         st.rerun() # Vuelve a ejecutar el script para refrescar

# --- Análisis y Visualización (Solo si hay datos) ---
if st.session_state.df is not None:
    df = st.session_state.df
    st.header("Vista Previa de los Datos")
    st.dataframe(df.head())

    st.header("Análisis Exploratorio")

    # Opciones en la sidebar
    st.sidebar.header("Opciones de Análisis")

    # Mostrar Información General
    if st.sidebar.checkbox("Mostrar Información del DataFrame (`df.info()`)", True):
        st.subheader("Información del DataFrame")
        # Capturar st.info() en un buffer de texto
        import io
        buffer = io.StringIO()
        df.info(buf=buffer)
        s = buffer.getvalue()
        st.text(s)

    # Mostrar Estadísticas Descriptivas
    if st.sidebar.checkbox("Mostrar Estadísticas Descriptivas (`df.describe()`)", True):
        st.subheader("Estadísticas Descriptivas")
        st.dataframe(df.describe())

    # Selección de Columnas para Visualización
    st.sidebar.subheader("Visualización")
    columnas_numericas = df.select_dtypes(include=np.number).columns.tolist()
    columnas_categoricas = df.select_dtypes(include='object').columns.tolist()

    if not columnas_numericas:
        st.sidebar.warning("No se encontraron columnas numéricas para graficar.")
    else:
        col_a_graficar_x = st.sidebar.selectbox("Selecciona la columna para el eje X", columnas_numericas)
        col_a_graficar_y = st.sidebar.selectbox("Selecciona la columna para el eje Y", columnas_numericas, index=min(1, len(columnas_numericas)-1)) # Segunda columna por defecto si existe

        tipo_grafico = st.sidebar.selectbox("Selecciona el tipo de gráfico", ["Dispersión (Scatter)", "Línea (Line)"])

        col_color = st.sidebar.selectbox("Selecciona columna para colorear (Opcional)", [None] + columnas_categoricas + columnas_numericas)


        # --- Generar Gráfico ---
        st.header("Visualización Personalizada")
        try:
            with st.spinner("Generando gráfico..."):
                if tipo_grafico == "Dispersión (Scatter)":
                    fig = px.scatter(df, x=col_a_graficar_x, y=col_a_graficar_y,
                                     color=col_color, title=f"Gráfico de Dispersión: {col_a_graficar_x} vs {col_a_graficar_y}")
                elif tipo_grafico == "Línea (Line)":
                     # Para gráfico de línea, usualmente se ordena por X si tiene sentido
                     df_sorted = df.sort_values(by=col_a_graficar_x) if col_a_graficar_x else df
                     fig = px.line(df_sorted, x=col_a_graficar_x, y=col_a_graficar_y,
                                   color=col_color, title=f"Gráfico de Línea: {col_a_graficar_x} vs {col_a_graficar_y}")

                st.plotly_chart(fig, use_container_width=True)
                st.success("Gráfico generado.")
        except Exception as e:
            st.error(f"No se pudo generar el gráfico: {e}")

else:
    st.info("Esperando a que cargues un archivo CSV.")

# --- Pie de página opcional ---
st.markdown("---")
st.caption("Creado con Streamlit por un AI Asistente")

```


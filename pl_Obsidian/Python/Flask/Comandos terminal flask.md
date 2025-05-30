
### instalar librerias a partir de requirements

-  pip install -r requirements.txt

### Crear variable FLASK_APP (en cmd o PS)
- export FLASK_APP=main.py    EN LINUX
-  set FLASK_APP=main.py         EN WINDOWS

## usar la variable en terminal de python
-  export FLASK_APP=main.py

### (OPCIONAL) enrutador
Este script de python evita el trabajo de crear la variable FLASK_APP :
```Python
from flask import Flask 
app = Flask(__name__) @app.route('/') 
def hello(): 
return 'Hello World Flask' 
	if __name__ == "__main__": 
	app.run(port=8080)
	```

### CORRER EL SERVIDOR
- flask run
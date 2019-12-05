
      
# <p style="text-align: right;"> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Flask_logo.svg/1200px-Flask_logo.svg.png" >    </p>


Flask es un “microframework” que permite crear aplicaciones web rápidamente y no requiere de herramientas o librerías particulares.

> Flask nació como una herramienta para conectar [wsgi](https://wsgi.readthedocs.io/en/latest/) con [jinja](https://jinja.palletsprojects.com/en/2.10.x/), y  ahora es uno de los web framework más famosos de python.

# Instalacion

Es recomendable instalar Flask en un [entorno virtual](https://virtualenv.pypa.io/en/latest/) y crear un entorno virtual para cada proyecto.
En caso de que tenga Python3, ya tiene instalado el entorno virtual por defecto: venv(Recomendado ya que es la version mas reciente).

## Crear un venv (Python3)
Vamos a crear el entorno virtual en la misma carpeta en la que ira en proyecto.

    Creamos la carpeta y dentro el venv:

    $ mkdir myproject
    $ cd myproject
    $ python3 -m venv venv

Una vez que lo creamos, cada vez que deseemos correr el proyecto vamos a tener que activarlo.

    Activar el venv:

    $ cd myproject
    $ source venv/bin/activate

Es recomendable utilizar la última versión de python 3. Flask soporta Python 3.5, Python 2.7 y PyPy

    Instalamos Flask:

    $ pip install Flask

Al instalar Flask, se instalaran algunas dependencias como Wsgi, Jinja, etc.

# Inicio Rapido: Hola Mundo!
Vamos a crear una pequeña y minimalista aplicacion web con Flask.

     from flask import Flask
     app = Flask(__name__)

     @app.route('/')
     def hello_world():
            return 'Hello, World!'


1. En la primera linea importamos Flask. Una instancia de esta clase va a ser nuestra aplicacion WSGI.

2. Luego creamos una instancia de esta clase. El primer argumento es el nombre del modulo o paquete de la aplicacion.

3. En el paso siguiente usamos el decorador __route()__ para decirle a Flask que URL tiene que ejecutar.

4. La funcion recibe un nombre que tambien se utiliza para generar URL para esa funcion en particular, y devuelve el mensaje que queremos mostrar en el navegador.

Asegurate de No llamar al archivo "Flask.py" porque estaria en conflicto con Flask.
Debes guardar el archivo en la misma carpeta en la cual creamos el entorno virtual.

# Correr nuestra app web

Para correr nuestra app y poder visualizarla en nuestro navegador, una vez activado el entorno virtual e instalado Flask, ejecutamos el siguiente comando en nuestra terminal:

    $ python3 nombre_archivo.py

Seguido de esto, abrimos nuestro navegador en la direccion http://127.0.0.1:5000/ y deberias ver tu Hola Mundo!

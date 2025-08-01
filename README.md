![LOGO ULEAD](https://github.com/user-attachments/assets/6f54a45a-9049-4952-8bd9-ffe2d4983bf3)

# **2025- II Programación Web**
# **Entregable grupal #3**

## Profesor: Alejandro Zamora Esquivel

Alumnos:
- Gabriel Corrales Mora.
- Jeralin Mayerlin Flores Hernández.
- Jean Rabbat Sánchez.


# **🌎 Explorador de Países**

## **DEMO:**


Un proyecto de aplicación web full-stack que permite a los usuarios explorar, buscar y guardar información sobre países de todo el mundo. La aplicación consume datos de la API pública [REST Countries](https://restcountries.com/) y utiliza una base de datos propia para gestionar la lista de países favoritos de cada usuario.

---

## ## Características

* **Exploración Global:** Visualiza una lista completa de países con sus banderas.
* **Búsqueda Dinámica:** Busca países específicos por su nombre.
* **Filtros Avanzados:** Filtra la lista de países por región (África, América, Asia, etc.) y subregión (Norteamérica, Caribe, etc.).
* **Detalles del País:** Haz clic en un país para ver información detallada como su capital, población, moneda e idioma principal.
* **Gestión de Favoritos:** Guarda tus países preferidos en una lista personalizada y elimínalos cuando quieras.
* **Interfaz Limpia y Responsiva:** Diseño moderno y adaptable a diferentes tamaños de pantalla.

---

## ## Tecnologías Utilizadas

Este proyecto está construido con las siguientes tecnologías:

* ### **Frontend**
    * **HTML:** Para la estructura semántica de la aplicación.
    * **CSS:** Para el diseño y la apariencia visual.
    * **JavaScript:** Para la interactividad, la manipulación del DOM y la comunicación con el backend.

* ### **Backend**
    * **Python:** Como lenguaje de programación del servidor.
    * **FastAPI:** Un framework web moderno y de alto rendimiento para construir APIs con Python.
    * **Uvicorn:** Como servidor ASGI para correr la aplicación FastAPI.

* ### **Base de Datos**
    * **MySQL:** Para almacenar la lista de países guardados por el usuario.

---

## ## Instalación y Puesta en Marcha

Para ejecutar este proyecto en tu máquina local, sigue estos pasos:

* ### **Prerrequisitos**
    Asegúrate de tener instalado:
    * Python 3.8 o superior
    * `pip` (el gestor de paquetes de Python)
    * Un servidor de MySQL en ejecución

* ### **1. Configuración del Backend**
    Primero, clona el repositorio y configura el servidor de Python.

    ```bash
    # 1. Clona el repositorio si lo tienes en Git
    git clone [<URL_DEL_REPOSITORIO>](https://github.com/Gab20031995/ExploradorDePaises.git)
    cd <NOMBRE_DE_LA_CARPETA>

    # 2. Crea y activa un entorno virtual (recomendado)
    python -m venv venv
    source venv/bin/activate  # En Windows usa: venv\Scripts\activate

    # 3. Instala las dependencias de Python
    pip install fastapi uvicorn mysql-connector-python httpx

    # 4. Configura la base de datos
    # Abre el archivo `main.py` y modifica el diccionario `DB_CONFIG`
    # con tus credenciales de MySQL.
    DB_CONFIG = {
        'host': "127.0.0.1", 
        'port': "tu puerto mysql",
        'user': "tu usuario mysql", 
        'password': "tu contraseña mysql",
        'database': "countries_db"
    }

    # 5. Inicia el servidor
    # La aplicación creará la base de datos y la tabla automáticamente.
    uvicorn main:app --reload
    ```
    El backend ahora estará corriendo en `http://127.0.0.1:8000`.

* ### **2. Iniciar el Frontend**
    Simplemente abre el archivo `index.html` en tu navegador web preferido. El JavaScript está configurado para comunicarse con el servidor local que acabas de iniciar.

---

## ## Estructura del Proyecto


├── index.html         # Archivo principal de la interfaz

├── style.css          # Hoja de estilos

├── script.js          # Lógica del frontend y llamadas a la API

├── main.py            # Servidor backend con FastAPI y lógica de negocio

└── README.md          # Este archivo

<p align="center">
<img src="/portada-repo.jpg" alt="1" border="0">
</p>
<p align="center">&nbsp;</p>

PRUEBA

prueba 2

# PREPARACIÓN ENTORNO LOCAL

## **Índice**

* [1. Configurar XAMPP](#1)
* [2. Configurar WORDPRESS en local](#2)
  - [2.1. Datos para la Configuración DB](#21)
  - [2.2. Datos para la Configuración del Tema](#22)
  - [2.3. Configurar WOOCOMMERCE](#23)
* [3. Configuración de Variables de Entorno](#3)
* [4. Instalación POSTGRESQL](#4)
* [5. Instalación DBEAVER](#5)
* [6. Iniciar el Servidor en local](#6)

## **1. Configurar XAMPP** <div id="1"/>

Instalar XAMPP [https://www.apachefriends.org/es/index.html](https://www.apachefriends.org/es/index.html)

Iniciar Servidor Apache en XAMPP

Iniciar Servidor MySQL en XAMPP

Crear Base de Datos con PHPMyAdmin en XAMPP

```
NOMBRE DE BASE DE DATOS: "oberon-lambda"
```

## 2. **Configurar WORDPRESS en local** <div id="2"/>

Descargar Wordpres [https://es.wordpress.org/](https://es.wordpress.org/)

Crear una carpeta en /xamp/htdocs/ llamada hermenautas

Extraer archivos de Wordpress dentro de la carpeta /xamp/htdocs/hermenautas

Proceder a la Instalación de Wordpress accediendo a [http://localhost/hermenautas](http://localhost/hermenautas)

### 2.1. **Datos para la Configuración DB** <div id="21"/>

```
Nombre de la base de datos = "oberon-lambda"

Nombre de usuario = 'root'

Contraseña = null

Servidor de la base de datos = 'localhost'

Prefijo de tabla = wp\_
```

### 2.2. **Datos para la Configuración del Tema** <div id="22"/>

Descargar Theme: SAVOY en [https://themeforest.net/](https://themeforest.net/)

Instalar Theme: SAVOY Padre y Child

### 2.3 **Configurar WOOCOMMERCE** <div id="23"/>

Realizar los pasos básicos de instalación del tema Savoy

Asegurarse de contar con todos los productos DEMO de SAVOY

Dirigirse a WooCommerce > Ajustes > Avanzado > Generar Clave API

Obtener Clave del cliente

Obtener Clave secreta de cliente

## 3. **Configuración de Variables de Entorno** <div id="3"/>

Guardar todas estas variables en un archivo .env y colocar en el directorio raíz donde se encuentre
alojado en el Backend
```bash
## APOLLO SERVER CONFIG

PORT_DEV = 4000
PROD_URL = "https://example.com"

## APOLLO ROVER CONIFG

APOLLO_TELEMETRY_DISABLED = 1

## POSTGRESQL CONFIG DEVELOPMENT

USERNAME_POSTGRESQL = 'admin'

PASSWORD_POSTGRESQL = '6yfKUY45kiRUE8WsDV2NY4B8G7cUgZimp4RZqTFqYJbg'

DATABASE_POSTGRESQL = 'test-user'

HOST_POSTGRESQL = 'localhost'

DIALECT_POSTGRESQL = 'postgres'

## MYSQL CONFIG DEVELOPMENT

MYSQL_HOST = 'localhost'

MYSQL_USER = 'root'

MYSQL_PASSWORD = null

MYSQL_DATABASE = "oberon-lambda"

## KEY PASETO

SECRET_KEY = 'k3.secret.sx9aeVOVlHJ_kl79LRSGB3WI_vRLjwsgMDmP5YH2rqLj5nQS25cdSFXgLkp43ycu'

PUBLIC_KEY = 'k3.public.A0mp-P4J96B1sAmFtksjtnUEmy0mAVACJggpPMjprGN56H7VFP420VDW9zd_o2XhqQ'

## WOOCOMMERCE

WOO_CONSUMER_KEY_DEV = "ck_c36d0ca5c9d2830cf0c72370f08cc1921d37dea5"

WOO_CONSUMER_SECRET_DEV = "cs_132883ebf4270163093499dada975e49dd7b01f7"
```
## 4. **Instalación POSTGRESQL** <div id="4"/>

Descargar e Instalar PostgreSQL [https://www.postgresql.org/](https://www.postgresql.org/)

Establecer contraseña SuperUsuario

Acceder a PgAdmin 4

Introducir contraseña SuperUsuario

Crear usuario admin con contraseña

```
6yfKUY45kiRUE8WsDV2NY4B8G7cUgZimp4RZqTFqYJbg
```

Crear Base de Datos llamada test-user y Asignar admin como propietario de test-user

## 5. **Instalación DBEAVER** <div id="5"/>

Instalar DBeaver [https://dbeaver.io/](https://dbeaver.io/)

Acceder al programa y realizar nueva conexión insertando los siguientes datos:

```
Connect by: Host

Host: localhost

Port: 5432

Database: test-user

Authentication: Database Native

Nombre de usuario: admin

contraseña: 6yfKUY45kiRUE8WsDV2NY4B8G7cUgZimp4RZqTFqYJbg

check en save password locally
```

## 6. **Iniciar el Servidor en local** <div id="6"/>

Encender el servidor Apache XAMPP

Encender el servidor MySQL XAMPP

Corroborar que el servidor PostgreSQL está activo

Ejecutar comando

```bash
npm start
```

Verificar si las tablas cargan

Verificar si Apollo Server carga en puerto 4000

> ¡Se espera que ya se tenga instalado Docker y esté activo!

# Comandos básicos para iniciar con los Contenedores

![Docker Image](https://th.bing.com/th/id/R.a2f46e02ea8f7f8af6c6989687bd6b52?rik=WiqhmOrrNVgkCA&pid=ImgRaw&r=0)

___


## 1. Abrir o cerrar entrono de venv:

Se recomienda utilizar un entorno virtual para instalar los módulos del proyecto, para esto usaremos el módulo de Python llamado ***virtualenv***, los siguientes comandos los recomiendo ejecutar en **CMD** y no en **Powershell**.

#### Instalar virtualenv:

    pip install virtualenv

#### Crear el archivo virtualenv:

    virtualenv venv

#### Activar:

    .\venv\Scripts\activate.bat

#### Desactivar:

    .\venv\Scripts\deactivate.bat

## 2. Crear nuestra imagen:
    docker build -t {image_name} .
> Ejemplo: `docker build -t flaskapp .`

## 3. Ver nuestras imágenes:
    docker images

## 4. Ver contenedores:
    docker container ls

## 5. Correr nuestra imagen en la consola:
    docker run -it -p {local_port}:{container_port} {image_name}
> Ejemplo: `docker run -it -p 7000:9000 flaskapp`

## 6. Correr nuestra imagen como un proceso:
    docker run -it -p {local_port}:{container_port} -d {image_name}
> Ejemplo: `docker run -it -p 7000:9000 -d {image_name}`

___

## Ruta para verificar el estado de la aplicación

En ambos casos al correr en proyecto podremos acceder a él desde la ruta:

    localhost:{local_port}/api/v1/

El puerto que usarémos será el establecido en local, como en el ejemplo que sería **7000**

    localhost:7000/api/v1/

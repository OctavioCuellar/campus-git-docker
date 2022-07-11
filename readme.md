1. Crear Repositorio

Creamos el repositorio con el nombre <campus-git-docker> dentro del directorio con el mismo nombre
Utilizamos los siguientes comandos git para crearlo:

Inicializamos:

    git init

Agregamos los archivos (readme.md)
    
    git add .

Hacemos el 1er commit de los cambios realizados
    
    git commit -m "Primer commit para el repositorio"

Definimos la branch en la que vamos a trabajar

    git branch -M main

Agregamos el repositorio de manera remota

    git remote add origin https://github.com/OctavioCuellar/campus-git-docker.git

Hacemos el push a la rama deseada

    git push -u origin main

----------------------------
2. Docker Hello World!

Para bajar la imagen oficial de docker se utiliza el siguiente comando:
    
    docker pull hello-world

Para correr la imagen se utiliza:

    docker run hello-world

Al correr la imagen nos aparece el siguiente mensaje en la terminal:

    Hello from Docker!
    This message shows that your installation appears to be working correctly.

----------------------------
3. Docker/SQL Server

Primero debemos bajar la imagen de SQL Server con el comando siguiente:

    docker pull mcr.microsoft.com/mssql/server:2019-latest

Ahora para ejecutar se utiliza el siguiente comando cuidando de los parámetros:
    docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=P4ssw0rd!' -p 1433:1433 -v ${pwd}/data:/var/opt/mssql/data -v ${pwd}/log:/var/opt/mssql/log -v ${pwd}/secrets:/var/opt/mssql/secrets -d mcr.microsoft.com/mssql/server:2019-latest

Donde:
-e Son los parámetros de configuración
-p Son los puertos que vamos a utilizar
-v Define los directorios para guardar los datos de forma persistente
-d Manda el proceso a background en vez de en primer plano en la terminal

Comprobamos que los datos del contenedor sean persistentes, para eso hice la base de datos llamada <PruebaChida>.

----------------------------


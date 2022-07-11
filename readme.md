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


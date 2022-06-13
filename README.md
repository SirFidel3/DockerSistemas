# DockerSistemas
#1
Requisitos:
Tener instalado docker y docker compose.
Para instalar docker compose utilizaremos el siguiente comando :
 Invoke-WebRequest "https://github.com/docker/compose/releases/download/v2.5.0/docker-compose-Windows-x86_64.exe" -UseBasicParsing -OutFile $Env:ProgramFiles\Docker\docker-compose.exe
 ![image](https://user-images.githubusercontent.com/91744605/172452773-45f59d7c-7329-4ab2-8f36-64516d497038.png)

#Creamos el fichero docker-compose.yml
![image](https://user-images.githubusercontent.com/91744605/172453234-9464079e-e21b-4f87-af0b-4cc09d4ab2e9.png)

Y en nuestro docker-compose yml introducimos lo siguiente.

![image](https://user-images.githubusercontent.com/91744605/173447333-071d5f80-2ebd-4ff5-b7a3-3be27a1d7622.png)


Toda la configuracion de SQL, version, imagen que descargar, la base de datos que tiene que iniciar, y los puertos.
Utilizaremos PHP MyAdmin para tener un gestor de la base de datos, el nombre de la imagen, el puerto y el enviroment.
Y finalmente el Tomcat, añadiremos la imagen de Tomcat, la instruccion para desplegar el .WAR y un puerto libre para docker.

Despues colocaremos nuestro archivo .war del proyecto en el mismo y el script de creacion de la base de datos.
![image](https://user-images.githubusercontent.com/91744605/173444719-10799414-5c92-4a76-ac05-b01ecebbf5ae.png)

#3
El siguiente paso para el despliegue sera dirigirnos a la terminal en el directorio del docker-compose y realizaremos el comando "docker-compose up -d"
![image](https://user-images.githubusercontent.com/91744605/173447711-2b833e8a-a134-4932-9995-21cc1a2b7ede.png)

#4
Lo siguiente sera la subida de la imagen a dockerhub. 
Primero nos logeamos en docker con el comando docker login
![image](https://user-images.githubusercontent.com/91744605/173448924-a0c954a0-38c7-49b5-ac04-d46c28de4dd4.png)
Haremos uso del comando docker tag y del docker push para subir las imagenes

#5
En conclusion docker es una manera eficiente y sencilla para mantener nuestro servidor desplegado y funcionando correctamente.

# Installation of Postgresql and Pgadmin in Ubuntu.
### Follow the following commands.

1. First of all install Postgresql in Ubuntu 22.04.01:

Esta primera linea de comandos **sudo apt update** sirve para actulizar la lista de paquetes disponibles en el sitema, esto es importante porque, cuando se instala un nuevo software o se actualiza un paquete existente, es necesario tener la lista más reciente de paquetes disponibles para asegurarse de que se está obteniendo la versión más reciente de software.</br>
En resumen, el comando "sudo apt update" es esencial para mantener el sistema actualizado y asegurar una instalación y actualización de software sin problemas.
* sudo apt update

En la siguiente linea de comandos **sudo apt install postgresql postgresql-contrib** lo que vamos hacer es instalar el sistema de gestión de bases de datos **PostgreSQL** y algunas herramientas adicionales llamadas **"contribuciones"**
* sudo apt install postgresql postgresql-contrib

Con esta linea de comandos **sudo su - postgres** vamos a cambiar el usuario actual del sistema a **"postgres"**, que es el nombre de usuario predeterminado para el usuario principal del sistema de gestión de bases de datos **PostgreSQL**.</br>
El comando **"sudo"** permite ejecutar la siguiente orden como superusuario, lo que significa que se tiene acceso a todos los comandos y archivos del sistema.</br>
El comando **"su"** (que significa **"switch user"**) permite cambiar el usuario actual del sistema.</br>
El parámetro **"- postgres"** indica que se desea cambiar el usuario actual a **"postgres"**.
* sudo su - postgres

Con el comando **psql** conectamos a una base de datos de PostgreSQL.
* psql

Luego de conectarse a la base de datos creamos un nuevo usuario llamado **admin** con la constraseña: 12345.
* create user **admin** with password **'12345.'**;

Luego creamos una base de datos con el siguiente comando, utilizando el usuario **admin**
* create database **my_first_DB** with owner **admin**;

Con esta linea de comandos vamos a darle privilegios de superUsuario al usuario **admin**
* alter user **admin** with superuser;

Si deseamos quitar o poner privilegios podemos utilizar los siguientes comandos:</br>
ALTER ROLE nombre_del_usuario NOSUPERUSER;</br>
ALTER ROLE nombre_del_usuario SUPERUSER;</br>
Y asi de facil podemos poner o quitar esos privilegios.</br>

Les dejo los siguientes comandos que le pueden ser muy utiles:

Con este comando podemos ver los usuarios de PostgreSQL.
* \du

Con este comando muestra una lista de todas las bases de datos disponibles en el servidor de PostgreSQL al que está conectado psql.
* \l

Y con la esta otra linea de comandos es similar pero muestra más información sobre cada base de datos.</br> Además de los detalles mostrados por \l, \l+ también muestra el tamaño de cada base de datos en bytes y el número de tablas y vistas que contiene.
* \l+



2. The second step is install pgadmin4:
* sudo apt install curl
* curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

* sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

* sudo apt install **pgadmin4**

### Finally, we open pgAdmin in the applications of ubuntu. 

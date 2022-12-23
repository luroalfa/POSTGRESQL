# Installation of Postgresql and Pgadmin in Ubuntu.
### Follow the following commands.

1. First of all install Postgresql in Ubuntu 22.04.01:

Esta primera linea de comandos **sudo apt update** sirve para actulizar la lista de paquetes disponibles en el sitema, esto es importante porque, cuando se instala un nuevo software o se actualiza un paquete existente, es necesario tener la lista más reciente de paquetes disponibles para asegurarse de que se está obteniendo la versión más reciente de software.</br>
En resumen, el comando "sudo apt update" es esencial para mantener el sistema actualizado y asegurar una instalación y actualización de software sin problemas.
* sudo apt update

En la siguiente linea de comandos **sudo apt install postgresql postgresql-contrib** lo que vamos hacer es instalar el sistema de gestión de bases de datos **PostgreSQL** y algunas herramientas adicionales llamadas **"contribuciones"**
* sudo apt install postgresql postgresql-contrib
* sudo su - postgres
* psql
* create user **admin** with password **'12345.'**;
* create database **my_first_DB** with owner **admin**;
* alter user **admin** with superuser;

2. The second step is install pgadmin4:
* sudo apt install curl
* curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

* sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

* sudo apt install **pgadmin4**

### Finally, we open pgAdmin in the applications of ubuntu. 

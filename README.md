# Installation of Postgresql and Pgadmin in Ubuntu.
### Follow the following commands.

1. First of all install Postgresql in Ubuntu 22.04.01:  
* sudo apt update
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

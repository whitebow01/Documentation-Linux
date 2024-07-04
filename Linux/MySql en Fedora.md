Buscar la distribucion que tengas:
https://dev.mysql.com/downloads/repo/yum/ 

## Puedes clickear encima o desde comando:
~~~
sudo dnf install <path to downloaded rpm>
~~~

## Instalamos MySQL
~~~
sudo dnf install mysql-community-server
~~~

## Start MySQL Service and Enable at Loggin:
~~~
sudo systemctl start mysqld
sudo systemctl stop mysqld

sudo systemctl enable mysqld
~~~

## find Default Password
Generará una key temporal para cambiarla al pass que quieras
~~~
sudo grep 'temporary password' /var/log/mysqld.log
~~~

## sudo grep 'temporary password' /var/log/mysqld.log
~~~
sudo mysql_secure_installation
~~~
Te pedirá la pas que temoral y luego agrega tu pass personal.

## Ingresar a mysql desde comando
Te pedirá tu pass para iniciar
~~~
sudo mysql -u root -p
~~~

## Removing MySQL
~~~
sudo rpm -e --nodeps mysql-community-libs mysql-community-common mysql-community-server
~~~


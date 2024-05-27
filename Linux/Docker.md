## Instalacion de docker

```
sudo pacman -Syu
sudo pacman -S docker
sudo systemctl start docker
sudo systemctl enable docker
```

Verificar que Docker esté funcionando correctamente:
```
sudo systemctl status docker
```

Agregar tu usuario al grupo de Docker (opcional pero recomendado)
Esto permite que puedas ejecutar comandos de Docker sin sudo.
```
sudo usermod -aG docker $USER
```
* * *
## Agregar una conexion a base de datos Oracle

`docker pull container-registry.oracle.com/database/free:latest`

Se te descargara una imagen 
`docker run -d --name "oracle-local" -p 1521:1521 -e ORACLE_PWD="password" container-registry.oracle.com/database/free:latest`
Cambia `password` por una clave que quieras
- Revisa la lista de imagenes y veras la que acabas de crear:

```
docker ps
```

Finalmente iniciamos conexion con sql:
1. Abremos sql y creamos una nueva conexion
- Usuario: system (ES el que tiene todos los beneficios)
- Password: La que pusieron anteriormente
En detalles:
- Cambiamos lo que dice `xe` por `free`

Probamos, guardamos y conectamos.

* * *
### COMANDOS PARA DOCKER 

Listar imágenes de Docker:
`docker images`
Listar contenedores en ejecución:
`docker ps`
Listar todos los contenedores (incluidos los detenidos):
`docker ps -a`
Detener un contenedor Docker en ejecución:
`docker stop nombre_del_contenedor`
Iniciar un contenedor Docker detenido:
`docker start nombre_del_contenedor`


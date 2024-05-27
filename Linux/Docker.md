## Instalacion de docker

sudo pacman -Syu
sudo pacman -S docker
sudo systemctl start docker
sudo systemctl enable docker

Verificar que Docker esté funcionando correctamente:
sudo systemctl status docker

Agregar tu usuario al grupo de Docker (opcional pero recomendado)
Esto permite que puedas ejecutar comandos de Docker sin sudo.
sudo usermod -aG docker $USER

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
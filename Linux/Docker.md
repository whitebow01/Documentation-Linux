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

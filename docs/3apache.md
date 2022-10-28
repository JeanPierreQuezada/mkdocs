# Instalando Apache Web Server

Vamos a instalar el servidor web apache en Ubuntu 22.04 LTS jammy Jellyfish desde los repositorios de la propia distribución, por lo que actualizamos.

    sudo apt update
![01](./images/apache01.png)

    sudo apt install apache2

Comprobamos el estado del servicio:

![02](./images/apache02.png)

El servicio queda escuchando peticiones para el protocolo http en el puerto 80 TCP, como podemos comprobar por comandos.

![03](./images/apache03.png)

Comando para saber la versión del servidor apache.

![04](./images/apache04.png)

Configuramos los permisos en el firewall para el servidor apache.

==Para http==

    sudo ufw allow http

==Para https==

    sudo ufw allow https

Probamos la configuración desde un navegador.

![05](./images/apache05.png)
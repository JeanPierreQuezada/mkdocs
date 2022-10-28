# Instalación de PHP 7.4 en Ubuntu

**Actualizamos Ubuntu**

    sudo apt update && sudo apt upgrade

**Instalar paquetes requeridos**

Las siguientes dependencias deberán instalarse para instalar PHP 7.4 con éxito. La mayoría de estos paquetes ya estarían presentes en su sistema, pero ejecutar el comando puede ayudar a garantizar que estén instalados.

    sudo apt install software-properties-common apt-transport-https -y

**Importar repositorio PHP Ondřej Surý**

Para empezar, importe el repositorio de PHP de Ondrej, quien ha sido un mantenedor de PHP para Debian durante más de una década y es ampliamente utilizado entre los servidores y usuarios de Ubuntu.
Importe el PPA usando el siguiente comando.

    sudo add-apt-repository ppa:ondrej/php -y

Una vez hecho esto, es bueno actualizar sus repositorios APT ya que el PPA puede traer actualizaciones adicionales a las dependencias existentes.

    sudo apt update

Después de importar el PPA y ejecutar una actualización, debería ver algunos paquetes que necesitan actualización; ejecute una actualización ahora.

    sudo apt upgrade

Luego:

    sudo apt-get install php7.4-mysqli

Posteriormente:

    sudo service apache2 restart

**Instalar PHP 7.4 con la opción Apache**

Si ejecuta una Servidor [Apache HTTP](https://httpd.apache.org/), usted puede ejecutar PHP como un módulo de Apache or PHP-FPM.

    sudo apt install php7.4 php7.4-common libapache2-mod-php7.4 php7.4-cli

Una vez completada la instalación, reinicie su servidor Apache para cargar el nuevo módulo PHP.

    sudo systemctl restart apache2

Creamos un archivo php para probar que esté operativo

```
vim /var/www/html/info.php
<?php
Phpinfo();
?>
```
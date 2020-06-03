# Práctica 3 Sockets Sistemas Distribuidos.

## Sobre este repositorio.
Cliente para la Práctica 3 de Sistemas Distribuidos para conectarse al servidor proporcionado.

## Requisitos Previos.
Instalar los siguientes paquetes en distribuciones Debian y derivados:
- ```expect```

Este paquete se puede encontrar en los repositorios oficiales de Debian y derivados (probado en Ubuntu 20.04 LTS):
```bash
sudo apt install expect -y 
```

Otros requisitos:
- ```awk```.
- ```md5sum```.
- ```base64```.
- ```nc```.

## Cómo utilizar el Cliente.
Después de instalar las dependencias mencionadas previamente, basta con asignarle permisos de **ejecución** al script ```expect```.

```bash
chmod +x client_msg.expect
```

La sintaxis del comando se muestra a continuación:
```bash
./client_msg.expect <ip_servidor> <puerto_servidor> <usuario> <puerto_local_udp>
```

Los parámetros son **obligatorios**, y se detallan a continuación:

- ```ip_servidor```: Dirección IP del servidor remoto.
- ```puerto_servidor```: Puerto del servidor remoto.
- ```usuario```: Nombre de usuario para conectarse al servidor.
- ```puerto_local_udp```: Puerto local del servidor ```nc``` para recibir la respuesta del servidor.

Para ejecutarlo, en el caso de mi usuario y los parámetros indicados por el instructor, se realizaría de la siguiente forma:
```bash
./client_msg.expect 192.168.24.1 10601 laguerrero.17 15000
```

**Nota:** El servidor ```nc``` es iniciado en el código del cliente, por lo que no es necesario crear una instancia previa.

## Documentación utilizada.
- https://linux.die.net/man/1/expect
- https://unix.stackexchange.com/questions/535750/expect-not-matching-server-response-string/535756#535756
- https://likegeeks.com/es/comando-expect/
- https://stackoverflow.com/questions/35968746/how-to-set-an-expect-variable-with-output-of-shell-command/35969382#35969382

## Autor.
Luis Guerrero.

## Licencia.
MIT.

TRABAJO PRACTICO INTREGRADOR-GRUPAL
ADMINISTRACION DE SISTEMAS
GNU/LINUX

- Gabriel Martinez Silva

-[Nombre Apellido 2]

-[Nombre Apellido 3]

-[Nombre Apellido 4]

-[Nombre Apellido 5]

DESCRIPCION:
Este repositorio contiene la solución al Trabajo Práctico Integrador Grupal de la materia, realizado en una máquina virtual Debian, siguiendo todas las consignas detalladas en el enunciado.

El trabajo abarca la instalación, configuración y administración de servicios esenciales en Linux, así como la gestión de almacenamiento, automatización de backups y documentación de la infraestructura.

REQUISITOS Y ENTORNO:

-Máquina virtual Debian provista por la cátedra.

-Importación mediante Oracle VirtualBox.

-Acceso root (clave: palermo).

-IP estática configurada en el mismo rango de red que la máquina física.


OBJETIVOS Y ESTRUCTURA DE TRABAJO:

1.Configuración del entorno:

-Blanqueo y cambio de clave root.

-Renombrado del hostname a TPServer.

2.Servicios:

-SSH: Acceso root vía autenticación con clave pública/privada.

-WEB: Instalación y configuración de Apache con soporte PHP 7.3+, sirviendo index.php y logo.png.

-Base de datos: Instalación y configuración de MariaDB, con carga del script db.sql.

3.Configuración de red:

Asignación de IP estática en el archivo de configuración, con los campos ADDRESS, NETMASK y GATEWAY.

4.Almacenamiento:

Adición de un disco extra de 10GB.

Dos particiones tipo 83:

/www_dir (3GB)

/backup_dir (6GB)

Montaje automático de ambos directorios.

Actualización de Apache para que apunte a /www_dir.

Redirección del contenido de /proc/partitions a un archivo persistente /proc/particion.

5.Backup:

Script backup_full.sh en /opt/scripts.

Permite indicar origen y destino por argumentos.

Nombra los archivos con formato nombre_bkp_YYYYMMDD.tar.gz.

Opción de ayuda (-help).

Validación de disponibilidad de origen y destino.

Automatización con cron:

Todos los días 00:00: backup de /var/logs.

Lunes, miércoles y viernes 23:00: backup de /www_dir.



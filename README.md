TRABAJO PRACTICO INTREGRADOR-GRUPAL
COMPUTACION APLICADA
GNU/LINUX

- Gabriel Martinez Silva

- Mateo Lorenzo Sauma

- Joaquin Arce Carrillo

-[Nombre Apellido 4]

-[Nombre Apellido 5]

DESCRIPCION:
Este proyecto es el resultado de un trabajo práctico grupal para la materia de Computacion Aplicada. Usamos una máquina virtual Debian ya configurada, y sobre esa base montamos y configuramos varios servicios esenciales que se suelen pedir en un entorno real.

¿Qué hicimos?
Configuración inicial:
Empezamos poniendo a punto la VM, cambiando la clave de root y dándole el nombre “TPServer” al host.

Servicios levantados:

SSH: configurado para que root pueda entrar usando llaves.

Servidor Web: instalamos Apache con soporte para PHP, y dejamos todo listo para servir los archivos index.php y logo.png.

Base de datos: usamos MariaDB, cargando el script de la cátedra.

Red:
Le pusimos IP fija a la máquina, con todos los parámetros para que funcione bien en la red local.

Almacenamiento:
Agregamos un disco nuevo y lo dividimos en dos particiones:

/www_dir (3GB), donde pusimos los archivos del sitio web.

/backup_dir (6GB), destinado a guardar los backups.
Ambos se montan automáticamente al arrancar.

Backups automáticos:
Programamos un script (backup_full.sh) que hace backups comprimidos de los directorios importantes, con nombre y fecha, y lo automatizamos para que se ejecute solo según el día y la hora.

Documentación y entregables:
Encontrás los archivos comprimidos de los directorios principales (/root, /etc, /opt, /proc, /www_dir, /backup_dir) y también el diagrama de la red que armamos.



¡Gracias por pasar! 😃


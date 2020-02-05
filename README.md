
Despliegue de un volumen distribuido con Gluster utilizando (two nodes)
========================================================================

Requisitos adicionales
======================

* 2 VM con sistema operativo RHEL 7.4 o superior 
* Se necesitan tener habilitados los siguientes Repositorios:
** rh-gluster-3-for-rhel-7-server-rpms
** rhel-7-server-ansible-2.9-rpms
* Almacenamiento
** Se requiere tener en ambos nodos un storage de igual capacidad.
*** Crear en el storage una particion con formato LVM
*** Crear un grupo de volumenes

**Automatizacion**
- Crear dos plays con sus roles respectivos en el formato de los playbooks de ALM Pandora.

**Pruebas a realizar**

- Crecer el FS. El crecimiento debera ser en caliente, sin necesidad de ventana.
- Pruebas desconectando uno de los nodos y validar la disponibilidad del servicio.
- Validar la gestion de permisos de usuario. (hacer pruebas)
- Levantar un APP contenerizado que use storage NFS.
- Migrar el NFS a Gluster para documentar el proceso (permisos etc) y hacer pruebas de disponibilidad


# Compute Engine

Google Compute Engine permite crear y ejecutar máquinas virtuales en la infraestructura de Google. 

Si tu activas el OS login lo que estas haciendo es dejar de utilizar la carpeta de .ssh de la instacia de compute engine para conectarte a esta y digamos que tienes la carpeta en el propio google, esto es un proceso mas seguro ya que asocias la clave pública a tu cuenta de google y así cuando accedes es como si te conectaras a la instancia, la cual es tu cuenta, y esta esta limitada solo a ciertos accesos según tus permisos.

datos:

compute.osAdminlogin: deja acceder a una instancia como si fuera administrador.

[MIG](Compute%20Engine%2028b5bd7c861081dea9a4c92056ce99be/MIG%2028b5bd7c8610817ebbb9f767d3b4aeb7.md)

La metadata de una instancia es tipo Json y se utiliza normalmente para poner valores como:

- Startup-script: a la hora de que se inicie la maquina.
- Variable de entorno para pasar configuración.
- Habilitar el OS login.
- O cosas sobre la versión de la app.

---
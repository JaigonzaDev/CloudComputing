# AWS Global Accelerator

Permite crear aceleradores para mejorar el rendimiento de las aplicaciones para usuarios locales y globales.

Hay dos tipos de aceleradores:

- Acelerador estandar que mejora la disponibilidad de las aplicaciones de internet. Dirige el tráfico de la red a los puntos de conexión de la región mas cercana al cliente.
- Acelerador de enrutamiento personalizado: puede asignar usuarios a un destino específico.

Se suele utilizar para:

- Escalar para aumentar la utilización de aplicaciones: imagina que tienes una aplicacion y tienes muchas instancias, pues puedes asignasr la ip estática a global accelerator o un servicio de DNS y este ya hace de load balancer entre las instancias.
- Aceleración para aplicaciones sensibles a la latencia: muchas aplicaciones como los videojuegos, medios, aplicaciones móviles, tecnología puglicitaria y finanzas requieren de poca latencia para esto global accelerator redirije a los usuarios al punto de conexión mas cercano lo que reduce la latencia, además reacciona rapidamente a los cambios de rendimiento de la red para mejorar el rendimiento.
- Recurperación ante desastres: si detecta que un punto de conexión esta fallando en la region principal activa al instante el redireccionamiento hacien el siguiente punto de conexión disponible.
- Protege sus aplicaciones: reduce el riesto de atque al ocultar el origen tras dos puntos de entra estáticos que estan protegidos con AWS Shield (DDOS)  y crea una conexión privada con la nube mediante direcciones de ip privadas lo que mantiene los load balancer fuera de internet.
- Mejroa el rendimiento para aplicaciones de VoIP y juegos en línea.
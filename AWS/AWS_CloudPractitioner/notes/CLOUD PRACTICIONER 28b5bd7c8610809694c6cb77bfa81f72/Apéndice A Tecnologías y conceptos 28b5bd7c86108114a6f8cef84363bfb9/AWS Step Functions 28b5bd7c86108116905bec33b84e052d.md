# AWS Step Functions

https://docs.aws.amazon.com/es_es/step-functions/latest/dg/welcome.html

¿Qué es?

AWS Step Functions es un servicio de orquestación que facilita la coordinación de componentes de aplicaciones distribuidas mediante la creación de flujos de trabajo visuales y gestionados. Permite diseñar, ejecutar y gestionar flujos de trabajo que conectan múltiples servicios de AWS en una secuencia lógica de pasos, lo cual es ideal para coordinar procesos complejos y automatizar tareas en la nube.

¿Como funciona?

Básicamente tu puedes definir los pasos que tiene que ocurrir cuando recive una señal indicada por ejemplo imagina que me llega un pedido (señal), activa el primer paso que es recibir el pedido y coger los datos llamando a un servicio de aws, el segundo paso es procesarlo invocando otro servicio y el tercero es enviar un mensaje de confirmación.

Info relacionada:

Una empresa necesita un servicio de flujo de trabajo visual con poco código que los desarrolladores puedan utilizar para crear aplicaciones distribuidas.

¿Qué servicio de AWS está diseñado para cumplir con estos requisitos?

A. AWS Step Functions
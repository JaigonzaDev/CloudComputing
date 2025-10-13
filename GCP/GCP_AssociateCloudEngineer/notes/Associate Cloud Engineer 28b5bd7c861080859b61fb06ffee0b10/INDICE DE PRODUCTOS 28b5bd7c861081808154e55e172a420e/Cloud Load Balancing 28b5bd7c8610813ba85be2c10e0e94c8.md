# Cloud Load Balancing

https://cloud.google.com/load-balancing/images/choose-lb.svg

Cloud Load Balancing actúa como un **punto de entrada único** (por ejemplo, una IP pública) que **redirige las peticiones entrantes** a los backends (tus servidores o servicios) más adecuados según distintos criterios:

- La ubicación del usuario
- El estado de los servidores
- La capacidad actual de cada uno
- El tipo de tráfico (HTTP, TCP, SSL, etc.)

🌐 **1. HTTP(S) Load Balancer (Global)**

🔐 **2. SSL Proxy Load Balancer (Global)**

🔁 **3. TCP Proxy Load Balancer (Global)**

🧱 **4. Internal Load Balancer**

🌐 **5. Network Load Balancer (L4 regional)**

**Anycast** es una técnica de red muy usada por servicios globales como Google, Cloudflare, AWS y otros para **hacer que una sola dirección IP esté disponible desde múltiples ubicaciones geográficas**, y que el tráfico sea automáticamente dirigido al **nodo más cercano o más óptimo** según la red del usuario.

### **Descarga de SSL**

La descarga de SSL te permite gestionar los certificados y el desencriptado de SSL de forma centralizada. Puedes habilitar el encriptado entre los backends y la capa de balanceo de carga para garantizar el nivel de seguridad más alto, con una sobrecarga añadida para el procesamiento en backends.

Cloud Logging registra todas las solicitudes que se envían a tu balanceador de carga. Estos registros sirven para depurar y analizar el tráfico de los usuarios. También puedes ver los registros de solicitudes y exportarlos a Cloud Storage, BigQuery o Pub/Sub para analizarlos.

| **Afinidad** | La afinidad de las sesiones de Cloud Load Balancing ofrece la posibilidad de dirigir y asignar el tráfico de los usuarios a instancias de backend específicas. |
| --- | --- |

| **Cloud Armor** | Las políticas de seguridad de [Google Cloud Armor](https://cloud.google.com/armor) te permiten limitar la frecuencia de las solicitudes de redirección a tu aplicación o tus balanceadores de carga de red en la rama de Google Cloud, lo más cerca posible de la fuente de tráfico entrante. |
| --- | --- |
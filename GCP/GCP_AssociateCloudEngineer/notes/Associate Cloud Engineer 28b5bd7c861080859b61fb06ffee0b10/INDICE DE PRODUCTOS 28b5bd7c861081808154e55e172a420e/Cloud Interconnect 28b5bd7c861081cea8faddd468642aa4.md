# Cloud Interconnect

Cloud Interconnect te permite conectar tu red de VPC a tu red local a través de una conexión física de alta velocidad.

| Tipo de Cloud Interconnect | Descripción |
| --- | --- |
| Interconexión dedicada | Proporciona conectividad entre tu red local y la de VPC a través de una conexión física directa entre tu red local y la de Google.
Para obtener más información, consulta la [descripción general de la interconexión dedicada](https://cloud.google.com/network-connectivity/docs/interconnect/concepts/dedicated-overview?hl=es-419). |
| Interconexión de socio | Proporciona conectividad entre tus redes locales y de VPC a través de un proveedor de servicios compatible.
Para obtener más información, consulta la [descripción general de la interconexión de socios](https://cloud.google.com/network-connectivity/docs/interconnect/concepts/partner-overview?hl=es-419). |
| Cross‑Cloud Interconnect | Proporciona conectividad entre tu red en otra nube y las redes de VPC a través de una conexión física directa entre la red de Google y la de otro proveedor de servicios en la nube.
Para obtener más información, consulta la [descripción general de Cross-Cloud Interconnect](https://cloud.google.com/network-connectivity/docs/interconnect/concepts/cci-overview?hl=es-419). |
| Interconexión entre sitios ([versión preliminar](https://cloud.google.com/products?hl=es-419#product-launch-stages)) | Proporciona conectividad entre los sitios de tu red local a través de conexiones físicas directas entre tus redes locales y la red de Google.
Para obtener más información, consulta la [descripción general de Cross-Site Interconnect](https://cloud.google.com/network-connectivity/docs/interconnect/concepts/cross-site-overview?hl=es-419). |

El tráfico entre tus redes no pasa por la Internet pública.

### Encripta el tráfico de Cloud Interconnect

Cloud Interconnect no encripta el tráfico de forma predeterminada. Puedes usar MACsec para Cloud Interconnect a fin de proteger el tráfico entre tu router local y los routers perimetrales de Google en circuitos compatibles de Cloud Interconnect.

https://cloud.google.com/network-connectivity/docs/interconnect/support/faq?hl=es-419
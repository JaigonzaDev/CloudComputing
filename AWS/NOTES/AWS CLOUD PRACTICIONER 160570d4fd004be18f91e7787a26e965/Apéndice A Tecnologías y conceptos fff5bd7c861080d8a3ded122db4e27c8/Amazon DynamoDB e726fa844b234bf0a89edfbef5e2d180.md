# Amazon DynamoDB

¿Qué es?

Amazon DynamoDB es una base de datos NoSQL sin servidor completamente administrada con un rendimiento de milisegundos de un solo dígito a cualquier escala.

DynamoDB ofrece un rendimiento uniforme en milisegundos de un solo dígito en un caso de uso de un carrito de la compra.

No permite la operación JOIN.

DynamoDB es ideal para casos de uso que requieren un rendimiento uniforme a cualquier escala con una sobrecarga operativa mínima o cero.

Las tablas globales proporcionan una solución completamente administrada para implementar una base de datos en varias regiones y multiactiva sin tener que crear ni mantener su propia solución de replicación. No asegura una consistencia global fuerte.

**Athena Federated Query** permite consultar DynamoDB con **SQL**

Time To Live (TTL) for DynamoDB is a cost-effective method for deleting items that are no longer relevant. TTL allows you to define a per-item expiration timestamp that indicates when an item is no longer needed. DynamoDB automatically deletes expired items within a few days of their expiration time, without consuming write throughput.
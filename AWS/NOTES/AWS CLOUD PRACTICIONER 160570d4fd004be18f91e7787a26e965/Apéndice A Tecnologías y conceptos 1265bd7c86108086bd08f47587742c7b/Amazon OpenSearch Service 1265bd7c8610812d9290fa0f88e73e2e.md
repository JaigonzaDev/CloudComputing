# Amazon OpenSearch Service

https://docs.aws.amazon.com/es_es/opensearch-service/latest/developerguide/what-is.html

¿Qué es?

**Amazon OpenSearch Service** (anteriormente conocido como Amazon Elasticsearch Service) es un servicio gestionado que facilita la implementación, operación y escalado de clústeres de OpenSearch y Elasticsearch en la nube de AWS. OpenSearch es un motor de búsqueda y análisis distribuido basado en Apache Lucene, diseñado para indexar, buscar y analizar grandes volúmenes de datos en tiempo real. Este servicio es ideal para casos de uso como la búsqueda de texto completo, el monitoreo de logs, la analítica de seguridad y la inteligencia de negocio.

¿Como funciona?

OpenSearch es una herramienta de analisis de datos que lo que hace es dividir los datos que le llegan en tokens estos tokens los indexa en distintos nodos para que puedan ser procesados rapidamente. Mas concretamente es normalizar esos tokens “Running” - “run” y guarda un puntero a donde esta en el documento, luego hace una indexación con los documentos que tienen esa tema relacionado sacando los documentos que tienen relación de manera eficiente.
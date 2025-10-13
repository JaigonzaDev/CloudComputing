# Amazon Aurora

https://docs.aws.amazon.com/es_es/AmazonRDS/latest/AuroraUserGuide/CHAP_AuroraOverview.html

¿Qué es?

**Amazon Aurora** es un servicio de base de datos relacional de alta disponibilidad, escalable y completamente administrado, diseñado para ofrecer la compatibilidad y las características de MySQL y PostgreSQL, pero con mejoras significativas en rendimiento y disponibilidad. Aurora es parte de la oferta de Amazon RDS (Relational Database Service) de AWS y está diseñado para combinar la simplicidad de las bases de datos relacionales con el rendimiento y la disponibilidad de bases de datos de alto nivel. Compatible con MySQL y PostgreSQL.

La Base de datos global de Amazon Aurora está diseñada para aplicaciones distribuidas globalmente, lo que permite que una sola base de datos de Amazon Aurora abarque múltiples regiones de AWS. Replica los datos sin afectar el rendimiento de la base de datos, permite lecturas locales rápidas con baja latencia en cada región y proporciona la recuperación de desastres de interrupciones en toda la región.

Las cargas de trabajo críticas con una huella global, como las aplicaciones financieras, de viaje o de videojuegos, tienen estrictos requisitos de disponibilidad y es posible que deban tolerar interrupciones en toda la región. La Base de datos global de Aurora utiliza una replicación basada en almacenamiento con una latencia típica inferior a 1 segundo mediante el uso de infraestructura exclusiva que permite que su base de datos quede completamente disponible para atender cargas de trabajo de las aplicaciones. En el caso improbable de que ocurra una degradación o interrupción regional, una de las regiones secundarias puede asumir capacidades de lectura y escritura en menos de 1 minuto.

Aurora viene con el escalado horizontal automático de forma nativa con PostgreSQL, también con Aurora Optimized Reads para postgreSQL permite la lectura para consultas complejas en PostgreSQL.

Aurora para mySQL permite el procesado paralelo. y tiene backtrack para aurora MySQL que permite restablecer un punto en concreto de la base de datos sin necesidad de hacer backups hasta 72 horas atrás.
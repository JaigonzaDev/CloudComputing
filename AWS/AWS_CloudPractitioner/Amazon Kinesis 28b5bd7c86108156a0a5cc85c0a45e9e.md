# Amazon Kinesis

https://docs.aws.amazon.com/es_es/streams/latest/dev/introduction.html

¿Qué es?

Amazon Kinesis es un servicio de AWS diseñado para facilitar la recopilación, procesamiento y análisis en tiempo real de grandes volúmenes de datos en streaming. Es ideal para aplicaciones que requieren analizar datos en movimiento casi en tiempo real, como análisis de eventos, monitoreo en vivo, y reacciones rápidas a datos.

¿Cómo funciona?

Básicamente hay tres servicios de Kinesis, Kinesis data stream lo que hace es almacenar en bufffers todos los datos que le llegan luego con kinesis data firehose puedes almacenar los datos en por ejemplo amazon S3 y por último con kinesis analytics puedes en el momento en el que los esta almacenando kinesis data stream analizar los datos dandole formato SQL.
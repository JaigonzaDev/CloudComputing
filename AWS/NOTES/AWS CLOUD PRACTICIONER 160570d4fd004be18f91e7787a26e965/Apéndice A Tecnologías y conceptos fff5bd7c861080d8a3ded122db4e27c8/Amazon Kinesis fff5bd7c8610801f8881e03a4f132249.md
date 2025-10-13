# Amazon Kinesis

https://docs.aws.amazon.com/es_es/streams/latest/dev/introduction.html

¿Qué es?

Amazon Kinesis es un servicio de AWS diseñado para facilitar la recopilación, procesamiento y análisis en tiempo real de grandes volúmenes de datos en streaming. Es ideal para aplicaciones que requieren analizar datos en movimiento casi en tiempo real, como análisis de eventos, monitoreo en vivo, y reacciones rápidas a datos.

¿Cómo funciona?

Básicamente hay tres servicios de Kinesis, Kinesis data stream lo que hace es almacenar en bufffers todos los datos que le llegan luego con kinesis data firehose puedes almacenar los datos en por ejemplo amazon S3 y por último con kinesis analytics puedes en el momento en el que los esta almacenando kinesis data stream analizar los datos dandole formato SQL.

### **🟢 Cuándo usar Kinesis Data Streams (KDS)**

✔ **Necesitas análisis en tiempo real** (baja latencia, <1 seg).

✔ **Quieres control total sobre el procesamiento** de los datos.

✔ **Vas a procesar datos en múltiples etapas** antes de almacenarlos.

✔ **Ejemplos:**

- Monitoreo en tiempo real de **aplicaciones o servidores** (logs en vivo).
- Procesamiento de eventos en **juegos en línea** (acciones de jugadores).
- **Transmisión de datos IoT** desde sensores conectados.
- **Análisis de fraude** en pagos con tarjetas.

---

### **🔵 Cuándo usar Kinesis Data Firehose (KDF)**

✔ **Solo necesitas almacenar los datos en un destino (S3, Redshift, etc.).**

✔ **No quieres escribir código** para procesar o transformar datos.

✔ **Quieres una solución administrada** sin preocuparte por shards o consumidores.

✔ **Ejemplos:**

- **Guardar logs centralizados en S3** desde múltiples fuentes (CloudWatch, Firewalls, etc.).
- **Almacenar eventos de usuarios** en Redshift para análisis.
- **Procesar datos de redes sociales** y enviarlos a Elasticsearch.
- **Convertir logs en formato Parquet** y comprimirlos automáticamente.

---

## **🚀 Resumen fácil**

- **Usa Kinesis Data Streams** → Si necesitas **procesamiento en tiempo real** y control.
- **Usa Kinesis Data Firehose** → Si solo quieres **almacenar y transformar datos sin esfuerzo**.
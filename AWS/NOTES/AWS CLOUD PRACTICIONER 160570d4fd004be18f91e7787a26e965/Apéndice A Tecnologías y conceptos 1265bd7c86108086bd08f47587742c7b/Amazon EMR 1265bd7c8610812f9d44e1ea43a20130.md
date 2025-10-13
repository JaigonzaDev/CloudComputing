# Amazon EMR

https://docs.aws.amazon.com/es_es/emr/latest/ManagementGuide/emr-what-is-emr.html

¿Qué es?

Amazon EMR (Elastic MapReduce) es un servicio administrado que facilita el procesamiento de grandes volúmenes de datos utilizando herramientas de big data populares como Apache Hadoop, Apache Spark, HBase, Presto, Flink, y otras. Amazon EMR es especialmente útil para realizar tareas de procesamiento distribuido como análisis de datos, indexación, machine learning, y transformación de datos.

¿Cómo funciona?

Básicamente para el tema de bigdata se necesita mucha capacidad, tanto de computo como de almacenamiento… Entonces EMR lo que hace es crear muchas instancias de EC2 (clusters) y los maneja como nodos ya que haciendo esto puede hacer distintos procesamientos a la vez, coordinandolos y luego uniendo los resultados. Al levantar instancias de EC2 es mucho más facil utilizar solo lo que se necesita por su flexibilidad y escalibilidad.
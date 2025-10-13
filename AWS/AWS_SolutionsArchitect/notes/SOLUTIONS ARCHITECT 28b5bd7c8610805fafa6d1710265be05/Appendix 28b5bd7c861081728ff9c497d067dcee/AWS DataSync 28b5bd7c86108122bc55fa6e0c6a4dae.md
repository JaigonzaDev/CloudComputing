# AWS DataSync

DataSync es un servicio de AWS que sirve para la transferencia online de data y como discovery service. Simplifica la transmision de datos de un forma rápida, facil y segura de tu archivo hacia, desde o entre los servicos de aws.

Funciona para los siguientes sistemas de archivos:

- Network File System (NFS).
- Server Message Block (SMB)
- Haddop Distributed File System (HDFS)
- Object storage.

Se suele utilizar para:

- Discover data: puede darte recomendaciones para migrar tus datos y también obtener datos de tu performance y utilización en on premises.
- Migrate data: puedes transferir data a través de la red a los Storage de AWS, incluye encriptación automáticay validacion de los datos para que llegue bien.
- Archive cold data: puedes mandarlo directamente a almecenamientos como S3 Glacier, Flexible Retrieval y S3 Hlacier Deep Archive.
- Replicate data: puedes copiar data en un s3. También puedes hacia EFS Fsx for windows, lustre y OpenZFS.
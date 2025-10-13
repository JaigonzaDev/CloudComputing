# AWS Storage Gateway

Storage Gateway ofrece a las aplicaciones un acceso local y en la nube a un almacenamiento en la nube practicamente ilimitado. Puede ser desplegado en tu entorno on-premises como una virtual machine (VMware ESXi, Microsoft Hyper-V, Linux KVM), en aws como un EC2, o como un hardware standalone. 

- Soportar protoclos como NFS, SMB, iSCSI VTL.
- Tine un cache local para acceder rapidamente a tus aplicaciones.
- Transferencia de datos seguros en tu entorno on premise y la nube.
- Se puede utilizar con tros servicios como s3, fsx, ebs y aws backup.
- Integración con servicos como KMS, IAM, CLoudTrail y cloudwatch.

Usos comunes esta mover backups al cloud, compartir una disco de almacenamiento como si estuviera en local pero realmente esta en la nube o para poveer a aplicaciones que funcionan on premises acceso con poca latencia a datos que estan en la nube.

Existen 4 tipos de Gateways:

- Amazon S3 File Gateway: te deja guardar data como objetos en S3 para data lackes, backups y machine learning workflows.
- Amazon FSx File Gateway: low-latency, te deja on primses, full access para sistemas de archivos, home directories para archvios compartidos.
- Tape Gateway: virtual tape library que se guarda en s3 para reemplazar tu infraestructura local de Tape. Cuando no requieres acceso inmediato o frecuente a tus tape puedes hacer que se elimine y puede pasarlo a s3 glacier o glacier deep archive apra reducir costes.
- Volume Gateway: te deja block storage columes por iSCSI, permite point-in-time buckups as EBS snapshots y se puede integrar con AWS backup.
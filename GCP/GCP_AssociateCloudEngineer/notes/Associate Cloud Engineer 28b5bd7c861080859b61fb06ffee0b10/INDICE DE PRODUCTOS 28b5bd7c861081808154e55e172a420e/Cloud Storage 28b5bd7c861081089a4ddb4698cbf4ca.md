# Cloud Storage

https://cloud.google.com/storage/docs/storage-classes?hl=es-419#coldline

Las siguientes funciones se aplican a todas las clases de almacenamiento:

- Almacenamiento ilimitado con acceso ilimitado.
- Carece de tamaño de objeto mínimo.
- Accesibilidad mundial y [ubicaciones de almacenamiento](https://cloud.google.com/storage/docs/locations?hl=es-419) en todo el mundo
- Latencia baja sin recuperación de datos sin conexión.
- [Garantiza alta durabilidad](https://cloud.google.com/storage/docs/availability-durability?hl=es-419#key-concepts) (99.999999999% de durabilidad anual).
- [Redundancia entre regiones](https://cloud.google.com/storage/docs/availability-durability?hl=es-419#cross-region-redundancy) cuando los datos se almacenan en una multirregional o múltiple.
- Una experiencia uniforme con las características, la seguridad, las herramientas y las API de Cloud Storage

- Standard
    - Retención Minima: Ninguna
    - Costo por Gb: Mas alto
    - Ideal para contenido activo.
- Nearline
    - Retención Minima: 30 días
    - Costo por Gb: Mas bajo que standard
    - Ideal para backups.
- Coldline
    - Retención Minima: 90 días
- Archive
    - Retención Minima: 365 días

## **Sí, todas las clases (Standard, Nearline, Coldline, Archive) tienen alta durabilidad**

Independientemente de la clase, Google Cloud Storage garantiza:

### 🛡️ **Durabilidad del 99.999999999% (11 nueves)**

Esto significa que, aunque pierdas una copia del archivo, habrá otras disponibles para restaurarlo. Esta durabilidad se logra gracias a la **replicación automática de datos**.

✅ **`SetStorageClass` es la forma recomendada de cambiar de clase** de almacenamiento: sin duplicar, sin mover, y mucho más eficiente.

## **Quieres cambiar la ubicación geográfica al mismo tiempo**

`SetStorageClass` **no cambia la ubicación** del objeto, solo su clase.

Si necesitas mover datos de:

- Una región a otra
- De una región a una multirregión (o viceversa)

… entonces **sí necesitas hacer una copia nueva**, porque:

- La ubicación de un objeto **no se puede cambiar**
- Tendrías que copiar el objeto a un nuevo bucket con la nueva ubicación y clase

---
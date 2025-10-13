# Cloud Key Management Service (KMS)

https://cloud.google.com/iap/docs/concepts-overview?hl=es-419

**Cloud KMS** (Key Management Service) es un servicio de Google Cloud que te permite:

- Crear, rotar y destruir **claves de cifrado**
- Usarlas para **cifrar/desencriptar datos**
- Controlar quién puede usar esas claves (con IAM)
- Ver registros de uso (auditoría)

Se usa para proteger datos **sensibles o confidenciales** (archivos, bases de datos, secretos, etc.) usando criptografía fuerte y controlada.

CMEK = Customer-Managed Encryption Keys

| Término | Significado |
| --- | --- |
| **DEK** | Clave usada para cifrar tus datos directamente |
| **KEK** | Clave usada para cifrar la DEK (está en Cloud KMS) |

**Autokey** es una función nueva que **automatiza todo el manejo de claves**.

Antes, tenías que:

- Crear un llavero
- Crear una clave
- Dar permisos
- Asociarla a tus recursos

Ahora, con **Autokey**, Google puede:

- Crear claves automáticamente cuando creás un recurso (ej: bucket)
- Asociarlas y configurarlas por vos

### **6. "También podés firmar o verificar firmas digitales con claves asimétricas o MAC."**

Cloud KMS no solo sirve para cifrar:

También podés usarlo para:

- **Firmar documentos o datos** (clave privada)
- **Verificar firmas** (clave pública)
- Usar **MACs (Message Authentication Codes)** para comprobar integridad de mensajes

🔐 Ejemplo práctico:

- Firmás un contrato digital con tu clave KMS.
- Otra persona puede verificar esa firma, sin acceso a tu clave privada.

| Opción | ¿Quién la controla? | ¿Qué permite? |
| --- | --- | --- |
| **CMEK** | Tú | Usás tus propias claves KMS para cifrar recursos |
| **CSEK** | Tú (clave externa manual) | Traés y cargas tu clave, no se guarda en GCP |
| **EKM** | Tú (clave vive *fuera* de GCP) | GCP *pide permiso* a tu sistema externo para cifrar/descifrar |

Todos los servicios estan de forma predeterminada encriptados por google, estas claves entiendo que forman parte de google y que no utilizan KMS, solo utilizarías KMS en el caso de que tu quieras encriptar algo en concreto con tu propia llave lo cual lo que podrías hacer es guardarla en KMS la llave privada y así ir encriptando los servicios que quieras con la llave pública correspondiente. Esta la posibilidad con CSEK que la cifres y uses CSEK que encriptas el servicio pero ya tendrías que desencriptarlo mediante algo externo. Y luego EKM es un servicio igual que el anterior pero que gestiona para que sea de forma automática
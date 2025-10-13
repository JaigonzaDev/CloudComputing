# Azure Key Vault

- **¿Qué es?** Azure Key Vault es un servicio en la nube centralizado para **almacenar y gestionar de forma segura secretos, claves criptográficas y certificados SSL/TLS**.
- **¿Cómo funciona?** Proporciona un almacén seguro para:
    - **Secretos:** Contraseñas de bases de datos, claves de API, cadenas de conexión, etc.
    - **Claves criptográficas:** Claves usadas para cifrado/descifrado de datos o firmas digitales.
    - **Certificados:** Certificados X.509 para sitios web, VPNs, etc.
- **Centralización:** Almacena todos tus secretos en un solo lugar seguro, facilitando la gestión y rotación.
- **Seguridad:** Los secretos se almacenan en módulos de seguridad de hardware (HSM) validados con FIPS (Federal Information Processing Standards) de nivel 2.
- **Control de acceso:** Puedes controlar estrictamente qué aplicaciones o usuarios tienen permiso para acceder a qué secretos específicos usando RBAC o políticas de acceso de Key Vault.
- **Auditoría:** Proporciona registros de auditoría de todas las operaciones realizadas en el Key Vault.
- **Reducción de riesgo:** Elimina la necesidad de almacenar secretos en código fuente, archivos de configuración o en repositorios públicos, que son prácticas de seguridad deficientes.
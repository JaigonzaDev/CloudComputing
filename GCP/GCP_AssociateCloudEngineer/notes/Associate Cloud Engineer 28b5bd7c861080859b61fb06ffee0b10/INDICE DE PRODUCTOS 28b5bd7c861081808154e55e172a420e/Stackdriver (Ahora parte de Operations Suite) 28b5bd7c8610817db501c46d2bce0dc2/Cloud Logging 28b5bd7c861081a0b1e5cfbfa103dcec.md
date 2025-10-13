# Cloud Logging

Sirve para registros de texto estructurado.

## 🔐 **1. Admin Activity audit logs** (Logs de Actividad Administrativa)

- **¿Qué registran?**
    
    Cambios **en la configuración** de los recursos.
    
    Ejemplos:
    
    - Crear o eliminar una VM
    - Cambiar permisos IM
    - Modificar una bucket de Cloud Storage
- **Importante:**
    
    Estos logs **siempre se generan**, no puedes desactivarlos ni excluirlos.
    
    Incluso si desactivas Cloud Logging, **Google sigue registrándolos** por seguridad.
    

---

## 📖 **2. Data Access audit logs** (Logs de Acceso a Datos)

- **¿Qué registran?**
    
    Accesos **a los datos en sí** o lectura de configuración.
    
    Ejemplos:
    
    - Leer datos de una tabla de BigQuery
    - Descargar un archivo de una bucket
    - Leer metadatos de una VM
- **¿Se generan por defecto?**
    - **NO**, están **desactivados por defecto**, excepto los de BigQuery.
    - ¿Por qué? Porque pueden generar **mucho volumen** y eso tiene coste.
- **¿Qué recursos NO generan estos logs?**
    
    Recursos públicos (acceso abierto para `allUsers` o `allAuthenticatedUsers`).
    
    Ejemplo: si tienes una bucket pública, no se registra quién accede.
    

---

## ⚙️ **3. System Event audit logs** (Logs de Eventos del Sistema)

- **¿Qué registran?**
    
    Cambios hechos automáticamente por Google Cloud, **no por usuarios**.
    
    Ejemplos:
    
    - Google reinicia tu VM por mantenimiento
    - Autoescalado de instancias
    - Actualizaciones automáticas de servicios
- **Importante:**
    
    Estos logs también **siempre se generan** y no se pueden desactivar.
    

---

## 🚫 **4. Policy Denied audit logs** (Logs de Políticas Denegadas)

- **¿Qué registran?**
    
    Cuando un acceso es **denegado** por una política de seguridad.
    
    Ejemplos:
    
    - Un usuario intenta borrar una VM pero no tiene permisos
    - Una función intenta acceder a un secreto, pero está bloqueado por una política de acceso
- **Importante:**
    - **Se generan por defecto**, y **sí tienen coste** por el almacenamiento.
    - No puedes evitar que se generen, pero **puedes excluirlos** del almacenamiento en Cloud Logging.
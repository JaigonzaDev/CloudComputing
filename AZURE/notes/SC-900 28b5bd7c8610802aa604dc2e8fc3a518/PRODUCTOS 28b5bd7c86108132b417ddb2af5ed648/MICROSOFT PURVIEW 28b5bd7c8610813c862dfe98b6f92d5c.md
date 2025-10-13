# MICROSOFT PURVIEW

- **Microsoft Service Trust Portal y principios de privacidad de Microsoft.**

**¿Qué es?** Es un portal público donde Microsoft proporciona información detallada sobre cómo protege los datos de los clientes y cómo cumple con varios estándares de cumplimiento.

**Propósito:** Sirve como una fuente centralizada de información sobre la **seguridad, privacidad y cumplimiento** de los servicios en la nube de Microsoft (como Azure, Microsoft 365, Dynamics 365, etc.). Aquí puedes encontrar:

- **Informes de auditoría de terceros:** Informes sobre certificaciones como ISO 27001, SOC 1/2/3, GDPR, etc.
- **Documentación de cumplimiento:** Guías, respuestas a preguntas frecuentes sobre cómo los servicios de Microsoft cumplen con normativas específicas.
- **Recursos de privacidad:** Información sobre cómo Microsoft maneja la privacidad de los datos.
- **Notificaciones de incidentes:** Aunque el principal punto es el estado del servicio de Azure, también se informan incidentes de seguridad importantes que afectan a la confianza del servicio.

**Principios de Privacidad de Microsoft:**

- **¿Qué son?** Son los compromisos fundamentales que Microsoft establece para la protección de la privacidad de los datos de los clientes en sus servicios. Se basan en leyes y marcos de privacidad globales.
- **Propósito:** Demuestran el enfoque de Microsoft en la privacidad de los datos y guían sus prácticas de desarrollo y operación de servicios. Estos principios a menudo incluyen:
    - **Control del cliente:** El cliente es dueño de sus datos y tiene control sobre ellos.
    - **Transparencia:** Microsoft es transparente sobre dónde se almacenan los datos y cómo se utilizan.
    - **Seguridad:** Microsoft invierte en seguridad para proteger los datos.
    - **Protección contra el acceso de terceros:** Microsoft no concede a terceros acceso directo o sin garantías legales a los datos de los clientes.
    - **Protección de la privacidad en todos los servicios:** La privacidad se integra en el diseño de los servicios.
    
- **Capacidades de administración de cumplimiento de Microsoft Purview:**
    - Clasificación de datos
    
    ### a. Clasificación de Datos
    
    - **¿Qué es?** Es el proceso de **identificar y categorizar la información** según su contenido, contexto y cómo se usa. Esto incluye identificar datos sensibles, como información de identificación personal (PII), información financiera o datos de salud.
    - **¿Cómo funciona en Purview?** Utiliza clasificadores integrados (ej., para números de tarjetas de crédito, números de seguro social) y clasificadores entrenables con aprendizaje automático para reconocer patrones en tus datos. Esto se integra con etiquetas de sensibilidad.
    - **Importancia:** Es el primer paso fundamental para proteger tus datos. No puedes proteger lo que no sabes que tienes.
    - Content explorer y Activity explorer
    
    ### b. Content Explorer y Activity Explorer
    
    - **Content Explorer:**
        - **¿Qué es?** Una herramienta que te permite **visualizar dónde se encuentran tus datos sensibles** clasificados dentro de Microsoft 365 (SharePoint Online, OneDrive para la Empresa, Exchange Online, Teams).
        - **Propósito:** Ofrece una vista detallada de la ubicación y el tipo de información sensible que posees, ayudando a identificar áreas de alto riesgo.
    - **Activity Explorer:**
        - **¿Qué es?** Una herramienta que te permite **auditar y visualizar las actividades de los usuarios** relacionadas con los datos sensibles.
        - **Propósito:** Puedes ver quién accedió a qué documento sensible, cuándo lo compartió, lo modificó o intentó realizar una acción prohibida. Es crucial para investigaciones y auditorías.
    - Etiquetas de sensibilidad y políticas de etiquetas de sensibilidad
    
    ### c. Etiquetas de Sensibilidad y Políticas de Etiquetas de Sensibilidad
    
    - **Etiquetas de Sensibilidad (Sensitivity Labels):**
        - **¿Qué son?** Son marcas persistentes que puedes aplicar a documentos y correos electrónicos (y otros elementos) para **clasificar su nivel de sensibilidad** (ej., "Público", "General", "Confidencial", "Altamente Confidencial").
        - **¿Cómo funcionan?** Una vez aplicada, la etiqueta viaja con el contenido. Permiten:
            - **Cifrado:** Cifrar automáticamente el contenido para que solo usuarios autorizados puedan verlo.
            - **Marcas de agua/Encabezados/Pies de página:** Añadir marcadores visuales al contenido.
            - **Restricciones de acceso:** Controlar quién puede copiar, imprimir o reenviar el contenido.
            - **Protección de contenedores:** Extender la protección a sitios de SharePoint o equipos de Teams.
        - **Aplicación:** Pueden ser aplicadas manualmente por los usuarios o automáticamente por políticas basadas en la clasificación de datos.
    - **Políticas de Etiquetas de Sensibilidad:**
        - **¿Qué son?** Son las reglas que definen cómo se publican y se aplican las etiquetas de sensibilidad a los usuarios.
        - **Propósito:** Asegurar que las etiquetas estén disponibles para los usuarios correctos y que las reglas de aplicación automática funcionen como se espera.
        
    - Prevención de pérdida de datos (DLP)
    
    ### d. Prevención de Pérdida de Datos (DLP - Data Loss Prevention)
    
    - **¿Qué es?** Las políticas DLP están diseñadas para **prevenir que la información sensible salga de tu organización** de forma no autorizada o accidental.
    - **¿Cómo funciona?** Las políticas DLP definen qué tipo de información sensible (ej., números de tarjeta de crédito, datos de clientes) no debe compartirse y en qué circunstancias. Pueden:
        - **Monitorear:** Auditar cuándo se intenta compartir información sensible.
        - **Bloquear:** Impedir que un correo electrónico con datos sensibles sea enviado fuera de la organización.
        - **Advertir al usuario:** Notificar al usuario que está intentando una acción de riesgo y permitirle anular la política (con justificación).
        - **Aplicar automáticamente etiquetas de sensibilidad.**
    - **Ámbitos:** Las políticas DLP se pueden aplicar en Exchange Online, SharePoint Online, OneDrive para la Empresa, Teams, dispositivos Windows 10/11, e incluso en aplicaciones SaaS de terceros a través de Defender for Cloud Apps.
    - **Importancia:** Es una defensa clave contra la exfiltración de datos y el cumplimiento de normativas como GDPR o HIPAA.
    
    - Administración de riesgos internos
    
    ### . Administración de Riesgos Internos (Insider Risk Management)
    
    - **¿Qué es?** Una solución que ayuda a las organizaciones a **detectar, investigar y actuar sobre actividades de riesgo de los usuarios internos** (empleados, contratistas). Se centra en el comportamiento de los usuarios que podría llevar a la pérdida de datos, fraude o acceso no autorizado.
    - **¿Cómo funciona?** Utiliza indicadores de actividad y aprendizaje automático para identificar patrones de riesgo. Puede detectar, por ejemplo:
        - Usuarios que acceden a datos sensibles a los que nunca antes habían accedido.
        - Descargas masivas de datos antes de una renuncia.
        - Exfiltración de datos a servicios de almacenamiento personal en la nube.
        - Actividad inusual de un usuario con acceso privilegiado.
    - **Propósito:** Proteger la organización de amenazas internas, tanto intencionales como no intencionales.
    
    - Soluciones de eDiscovery
    
    ### . Soluciones de eDiscovery
    
    - **¿Qué es?** Como ya vimos, eDiscovery (electronic discovery) es el proceso de **identificar, preservar, recopilar y presentar información electrónica** relevante para investigaciones legales, regulatorias o internas.
    - **Niveles en Purview:**
        - **eDiscovery (Standard):** Permite buscar contenido en ubicaciones de Microsoft 365 y aplicar retenciones legales (legal holds) para preservar los datos.
        - **eDiscovery (Premium):** Ofrece funcionalidades avanzadas como la gestión de custodios, flujos de trabajo de revisión, reducción de datos con IA, etc.
    - **Importancia:** Es esencial para responder a litigios y solicitudes de información de manera eficiente y conforme a la ley.
    
    - Capacidades de auditoría
    
    ### g. Capacidades de Auditoría
    
    - **¿Qué es?** Microsoft Purview proporciona **registros detallados de actividad (logs de auditoría)** de los usuarios y administradores en todos los servicios de Microsoft 365 y Azure.
    - **¿Cómo funciona?** Registra eventos como inicios de sesión, acceso a archivos, cambios de configuración, envío de correos electrónicos, etc. Estos registros son inmutables y se conservan durante un período definido (dependiendo de la licencia).
    - **Herramientas:** El **Registro de Auditoría Unificado** en el Portal de Cumplimiento permite buscar y exportar estos eventos.
    - **Importancia:** Es crucial para la **rendición de cuentas, la investigación forense, la solución de problemas y el cumplimiento normativo**. Permite responder a preguntas como "¿quién eliminó este archivo?" o "¿quién cambió esta configuración crítica?".
- **Capacidades de gobernanza de recursos en Azure.**

### h. Capacidades de Gobernanza de Recursos en Azure

Aunque Microsoft Purview es la suite principal para el cumplimiento de datos, las capacidades de gobernanza también se extienden a los recursos de Azure.

- **¿Qué es?** Se refiere a las herramientas y procesos para **gestionar, controlar y optimizar el uso de los recursos de Azure**.
- **Elementos clave (que ya hemos visto en otras secciones):**
    - **Azure Policy e Iniciativas:** Para asegurar que los recursos se creen y configuren según las reglas de la organización (ej., todas las VMs deben tener etiquetas, solo se pueden crear recursos en ciertas regiones).
    - **Azure Blueprints:** Para definir un conjunto repetible de recursos de Azure, políticas, roles y otros artefactos de forma declarativa.
    - **Control de Acceso Basado en Roles (Azure RBAC):** Para definir quién puede hacer qué en tus suscripciones y recursos de Azure.
    - **Grupos de Administración:** Para organizar tus suscripciones y aplicar políticas de forma jerárquica.
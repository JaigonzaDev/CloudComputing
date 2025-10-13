# MICROSOFT SENTINEL

- Conceptos de Security Information and Event Management (SIEM)
- Security Orchestration Automated Response (SOAR)
- Detección y mitigación de amenazas

**Microsoft Sentinel** es una solución de **Security Information and Event Management (SIEM) nativa de la nube y escalable, con capacidades de Security Orchestration Automated Response (SOAR).** Funciona como el cerebro de seguridad centralizado para tu organización en Azure y en entornos multicloud e híbridos.

Sí, podríamos simplificarlo y decir que **Microsoft Sentinel es un SIEM (Security Information and Event Management) potenciado por IA** que:

1. **Recopila y centraliza** una vasta cantidad de **datos de seguridad y eventos** de todas las fuentes conectadas a tu entorno (tu tenant de Microsoft, otras nubes, sistemas locales, aplicaciones, etc.). No es una IA en el sentido de una "mente" consciente, sino que **utiliza capacidades de inteligencia artificial y aprendizaje automático (ML)** para procesar y encontrar patrones en esos enormes volúmenes de datos.
2. A través de estas capacidades de IA/ML y **reglas de detección personalizadas o predefinidas**, **identifica y genera alertas** cuando detecta actividades o sucesos sospechosos que podrían indicar una amenaza o un incidente de seguridad.
3. Y sí, lo crucial es que integra **capacidades SOAR (Security Orchestration Automated Response)**. Esto significa que puedes **asignarle "playbooks" (libros de estrategias)**, que son flujos de trabajo automatizados, para que **gestione de forma automática** estas alertas. Esto puede ir desde notificar a tu equipo, bloquear una dirección IP maliciosa, deshabilitar una cuenta de usuario comprometida, o cualquier otra acción que definas para mitigar la amenaza de forma rápida y eficiente.
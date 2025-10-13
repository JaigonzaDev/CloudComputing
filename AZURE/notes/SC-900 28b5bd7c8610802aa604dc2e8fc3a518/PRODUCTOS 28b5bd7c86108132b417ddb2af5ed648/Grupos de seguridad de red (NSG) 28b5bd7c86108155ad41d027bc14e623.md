# Grupos de seguridad de red (NSG)

### Grupos de Seguridad de Red (NSG - Network Security Groups)

- **¿Qué son?** Los NSG son **filtros de tráfico de red básicos** que te permiten controlar el tráfico de entrada y salida a nivel de interfaz de red (NIC) o subred para recursos de Azure.
- **¿Cómo funciona?** Contienen una lista de **reglas de seguridad** que especifican si el tráfico es permitido o denegado, basándose en:
    - **Dirección de tráfico:** Entrada o salida.
    - **Prioridad:** Define el orden en que se evalúan las reglas.
    - **Origen/Destino:** Direcciones IP (individuales, rangos o etiquetas de servicio de Azure).
    - **Puerto de origen/destino.**
    - **Protocolo:** TCP, UDP, ICMP o cualquier.
    - **Acción:** Permitir o Denegar.
    - Las reglas se evalúan en orden de prioridad, y la primera regla que coincide determina la acción.
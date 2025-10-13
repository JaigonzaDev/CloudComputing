# Web Application Firewall (WAF)

- **¿Qué es?** Un WAF es un tipo de firewall diseñado específicamente para **proteger las aplicaciones web** de ataques comunes basados en la web.
- **¿Cómo funciona?** A diferencia de un firewall de red (como Azure Firewall) que opera a nivel de red, un WAF inspecciona el tráfico HTTP/HTTPS (capa de aplicación - Capa 7 del modelo OSI). Detecta y bloquea ataques que explotan vulnerabilidades comunes de aplicaciones web, como:
- Inyección SQL (SQL Injection).
- Cross-Site Scripting (XSS).
- Falsificación de Solicitudes entre Sitios (CSRF).
- Inclusión de Archivos Locales/Remotos.
- Ataques de Bots y escáneres vulnerables.
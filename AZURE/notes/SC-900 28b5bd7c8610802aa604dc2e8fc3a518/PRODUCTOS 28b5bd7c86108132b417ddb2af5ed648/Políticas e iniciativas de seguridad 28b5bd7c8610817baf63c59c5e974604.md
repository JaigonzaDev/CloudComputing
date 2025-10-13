# Políticas e iniciativas de seguridad

### 1. Azure Policy

- **¿Qué es?** Azure Policy es un servicio que te permite **crear, asignar y gestionar políticas** que aplican reglas y efectos sobre tus recursos de Azure. Estas políticas pueden auditar tus recursos en busca de incumplimientos, impedir la creación de recursos que no cumplan, o incluso modificar recursos para que cumplan automáticamente.

**Propósito:**

- **Imponer estándares:** Asegurar que los recursos se desplieguen y se configuren de acuerdo con las directrices de tu empresa (ej., todos los discos de VM deben estar cifrados).
- **Mantener el cumplimiento:** Demostrar que tus recursos cumplen con estándares regulatorios (ej., HIPAA, PCI DSS).
- **Prevenir errores:** Evitar que los usuarios desplieguen recursos en regiones no autorizadas o utilicen tamaños de VM no aprobados.
- **Automatizar la seguridad:** Corregir automáticamente configuraciones erróneas o añadir etiquetas obligatorias.

**Asignaciones de Política:**

Vinculan una definición de política (o una iniciativa, que veremos a continuación) a un

**ámbito específico**

. El ámbito puede ser:

- Un **grupo de administración** (varias suscripciones).
- Una **suscripción** completa.
- Un **grupo de recursos**.
- Un **recurso individual**.
- Las políticas se heredan hacia abajo en la jerarquía.

### 2. Iniciativas de Política (Policy Initiatives)

- **¿Qué son?** Una **iniciativa de política** (a menudo llamada simplemente "iniciativa") es una **colección de definiciones de política** agrupadas para lograr un objetivo de cumplimiento más amplio.
- **Propósito:** Simplifican la gestión y la asignación de políticas. En lugar de asignar decenas de políticas individuales para cumplir con un estándar, puedes asignar una sola iniciativa.
- **Ejemplo:** Una iniciativa para el cumplimiento de **PCI DSS** (Payment Card Industry Data Security Standard) podría incluir políticas individuales para:
    - Cifrar todos los datos sensibles.
    - Requerir MFA para el acceso administrativo.
    - Asegurar que los NSG limiten el tráfico a puertos específicos.
    - Deshabilitar el acceso RDP directo a Internet.
    - Monitorear la actividad de red.
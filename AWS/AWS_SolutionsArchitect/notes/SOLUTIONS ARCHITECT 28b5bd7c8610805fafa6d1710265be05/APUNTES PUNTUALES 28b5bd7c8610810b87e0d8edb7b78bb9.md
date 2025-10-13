# APUNTES PUNTUALES

Un **Cluster Placement Group** (CPG) es una estrategia de agrupamiento que AWS utiliza para colocar un conjunto de instancias EC2 físicamente cerca unas de otras en el mismo hardware subyacente dentro de una misma **Zona de Disponibilidad**.

### **Características clave**:

- **Baja latencia**: Al estar en hardware cercano, se minimiza la latencia de red entre las instancias.
- **Alto rendimiento de red**: Las instancias pueden aprovechar mayores tasas de transferencia de datos.
- **Limitación de ubicación**: Las instancias deben ser compatibles con esta agrupación y estar disponibles en la misma Zona de Disponibilidad.

Un **Spread Placement Group** es otra estrategia de agrupamiento de AWS que **distribuye las instancias EC2 en hardware físico diferente**. Esto minimiza el impacto de fallos de hardware en un único nodo.

### **Características clave**:

- **Alta tolerancia a fallos**: Si una máquina falla, solo afecta una instancia.
- **Limitación en la cantidad de instancias por nodo físico**: AWS permite un máximo de 7 instancias por grupo por Zona de Disponibilidad.
- **Mayor latencia**: Al distribuir las instancias en múltiples nodos, aumenta la latencia en la comunicación.

---

it is a best practice to use **IAM roles for tasks** to grant permissions to AWS resources

---

El **active-active failover** es un modelo de configuración de alta disponibilidad en el que **varias instancias o regiones están activas simultáneamente**, y todas pueden recibir tráfico al mismo tiempo. Este enfoque distribuye las solicitudes entrantes entre los endpoints activos, lo que puede mejorar el rendimiento, reducir la latencia y proporcionar tolerancia a fallos.

---

S3 Object Lock in compliance mode ensures that the objects are immutable and cannot be deleted or modified by anyone for the specified retention period.
Maximum Resiliency: Both S3 Standard and S3 Glacier Deep Archive offer high durability of 99.999999999% (11 9's).

---

Un **Elastic Inference Accelerator** es un servicio de AWS diseñado específicamente para optimizar el costo y el rendimiento de las aplicaciones de **machine learning (ML)**, particularmente para las tareas de **inferencia de modelos de ML**. Aquí tienes una explicación más clara:

---

El término **"idle"** en el contexto de **Amazon RDS** (y en general en servicios de computación en la nube) significa que una **instancia de base de datos está inactiva** o **no está siendo utilizada activamente**.

---

**Canary release** es la forma más segura de desplegar nuevas versiones sin afectar a todos los usuarios a la vez. Permite realizar pruebas de la nueva versión con un porcentaje de tráfico antes de redirigir todo el tráfico. Esto asegura que no haya problemas graves y permite un cambio suave a la nueva versión de la API.

---

**"Coupling"** (o acoplamiento) se refiere al grado de dependencia que existe entre los diferentes componentes o módulos de un sistema. En el contexto del diseño de software y arquitectura de aplicaciones, el acoplamiento se refiere a qué tan dependientes están entre sí los diferentes módulos, servicios o componentes.

---

Una **Event-Driven Architecture** (Arquitectura basada en eventos) es un patrón de diseño en el que los sistemas se comunican y reaccionan a eventos en lugar de seguir flujos lineales o sincronizados.

---

Un **State Machine** (máquina de estados) es una herramienta para diseñar y gestionar flujos de trabajo complejos en AWS **Step Functions**. Una máquina de estados representa un flujo de trabajo como una serie de pasos (o estados) conectados. Cada estado tiene una función específica y puede realizar acciones, tomar decisiones, esperar entradas o manejar errores.

---

Un **Rolling Deployment Policy** (Política de Despliegue Rodante) es una estrategia de despliegue utilizada para actualizar aplicaciones en un entorno de producción sin tiempo de inactividad (**zero downtime**) o con interrupciones mínimas.

---

Provisioned concurrency – This is the number of pre-initialized execution environments allocated to your function. These execution environments are ready to respond immediately to incoming function requests. Provisioned concurrency is useful for reducing cold start latencies for functions. Configuring provisioned concurrency incurs additional charges to your AWS account.
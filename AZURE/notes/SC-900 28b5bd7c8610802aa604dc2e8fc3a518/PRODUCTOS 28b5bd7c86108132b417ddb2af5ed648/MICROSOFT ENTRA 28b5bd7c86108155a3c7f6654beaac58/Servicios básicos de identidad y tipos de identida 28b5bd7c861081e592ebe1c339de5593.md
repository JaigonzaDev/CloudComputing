# Servicios básicos de identidad y tipos de identidad

Existen tres categorías.

**Usuario**

Puede asignar identidades a personas (humanos). Algunos ejemplos de identidades asignadas a personas son los empleados de una organización que suelen configurarse como usuarios internos, y los usuarios externos como clientes, consultores, proveedores y asociados. Para nuestros fines, nos referiremos a ellas como identidades de usuario. 

- Puede ser interna o externa: La autenticación interna significa que el usuario tiene una cuenta en Microsoft Entra ID de la organización de host y usa esa cuenta para autenticarse en Microsoft Entra ID. La autenticación externa significa que el usuario se autentica mediante una cuenta de Microsoft Entra externa que pertenece a otra organización, una identidad de red social u otro proveedor de identidades externo.
    - Miembro interno: estos usuarios suelen considerarse empleados de su organización.
    - Invitado externo: usuarios externos o invitados, incluidos consultores, proveedores y asociados
    - Miembro externo: este escenario es común en las organizaciones que constan de varios inquilinos. Tenga en cuenta el escenario en el que el inquilino de Microsoft Entra de Contoso y el inquilino de Microsoft Entra de Fabrikam son inquilinos de una organización grande. Los usuarios del inquilino de Contoso necesitan acceso de nivel de miembro a los recursos de Fabrikam. En este escenario, los usuarios de Contoso se configuran en el directorio de Microsoft Entra de Fabrikam, de modo que se autentican con su cuenta de Contoso, que es externa a Fabrikam, pero tienen un userType de miembro para habilitar el acceso de nivel de miembro a los recursos de la organización de Fabrikam.
    - Invitado interno: este escenario existe cuando las organizaciones que colaboran con distribuidores, proveedores y vendedores configuran cuentas de Microsoft Entra internas para estos usuarios, pero las designan como invitados estableciendo el objeto de usuario UserType en Invitado. Como invitado, tienen permisos reducidos en el directorio. Esto se considera un escenario heredado, ya que ahora es más común usar la colaboración B2B. Con la colaboración B2B, los usuarios pueden utilizar sus propias credenciales, permitiendo que su proveedor de identidades externo administre la autenticación y el ciclo de vida de su cuenta.

**Identidades de Carga de Trabajo (Workload Identities) y su relación con Identidades Administradas (Managed Identities)**

"Identidad de Carga de Trabajo" es un término más amplio que se refiere a cualquier identidad que no sea humana (aplicaciones, servicios, scripts, etc.) que necesita autenticarse y acceder a recursos. Los Registros de Aplicaciones y las Entidades de Servicio son la base para esto.

puede asignar identidades a objetos basados en software, como aplicaciones, máquinas virtuales, servicios y contenedores. Estas identidades se denominan identidades de carga de trabajo.

**Registros de Aplicaciones (App Registrations)** y **Entidades de Servicio (Service Principals)**

Las **Identidades Administradas (Managed Identities)** son una **característica específica de Azure** que simplifica drásticamente la gestión de las credenciales para las identidades de carga de trabajo *que se ejecutan dentro de Azure*.

### **Identidades administradas**

Las identidades administradas son un tipo de entidad de servicio que se administran de forma automática en Microsoft Entra ID y eliminan la necesidad de que los desarrolladores administren las credenciales. Las identidades administradas proporcionan una identidad para que la usen las aplicaciones al conectarse a recursos de Azure compatibles con la autenticación de Microsoft Entra, sin costo adicional.

**Dispositivo**

Puede asignar identidades a dispositivos físicos, como teléfonos móviles, equipos de escritorio y dispositivos IoT.

**Grupos**

Los grupos se usan para conceder permisos de acceso a todos los miembros del grupo, en lugar de tener que asignar derechos de acceso individualmente

Hay dos tipos de grupo:

- Seguridad(Dispositivos en concreto): un grupo de seguridad es el tipo de grupo más común y se usa para administrar el acceso de usuario y dispositivo a los recursos compartidos. Por ejemplo, puede crear un grupo de seguridad para una directiva de seguridad específica, como el autoservicio de restablecimiento de contraseña o para su uso con una directiva de acceso condicional para requerir MFA. Los miembros de un grupo de seguridad pueden incluir usuarios (incluidos usuarios externos), dispositivos, otros grupos y entidades de servicio. La creación de grupos de seguridad requiere un rol de administrador de Microsoft Entra.
- Microsoft 365 (colaboracion): un grupo de Microsoft 365, que también se conoce como grupo de distribución, se usa para agrupar usuarios según las necesidades de colaboración. Por ejemplo, puede conceder a los miembros del grupo acceso a un buzón compartido, a un calendario, a archivos de sitios de SharePoint, etc. Los miembros de un grupo de Microsoft 365 solo pueden incluir usuarios, incluidos los usuarios fuera de su organización. Dado que los grupos de Microsoft 365 están diseñados para la colaboración, por defecto se permite a los usuarios crear grupos de Microsoft 365, por lo que no necesita un rol de administrador.
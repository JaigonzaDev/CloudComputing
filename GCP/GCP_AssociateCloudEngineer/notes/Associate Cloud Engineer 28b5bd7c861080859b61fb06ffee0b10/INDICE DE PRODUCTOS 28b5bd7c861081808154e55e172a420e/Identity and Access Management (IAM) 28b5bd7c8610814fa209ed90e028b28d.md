# Identity and Access Management (IAM)

https://cloud.google.com/iam/docs/overview?hl=es-419

IAM primero verifica si tiene los permisos necesarios. Si no es así, IAM impedirá que realice la acción.

Otorgar permisos a alguien en IAM implica los siguientes tres componentes:

- **Principal**: Es la identidad de la persona o el sistema al que deseas otorgar permisos.
- **Rol**: Es la colección de permisos que deseas otorgar al principal.
- **Recurso**: Es el Google Cloud recurso al que deseas permitir que acceda el principal.

Se pueden aplicar en cuatro niveles:

- Organización
- Carpetas
- Proyectos
- Recursos individuales

gcloud iam roles copy command

## Cómo funciona la identidad temporal como cuenta de servicio

La identidad temporal como cuenta de servicio siempre involucra dos identidades: una principal autenticada y la cuenta de servicio que suplanta la principal. Para actuar en nombre de la cuenta de servicio, la principal autenticada obtiene un token para la cuenta de servicio y, luego, lo usa para autenticarse como la cuenta de servicio.

A diferencia de los usuarios normales, las cuentas de servicio no tienen contraseñas. En su lugar, las cuentas de servicio usan pares de claves RSA para la autenticación: si conoces la clave privada del par de claves de una cuenta de servicio, puedes usar la clave privada para [crear un token del portador de JWT](https://developers.google.com/identity/protocols/oauth2/service-account?hl=es-419#httprest) y usar el token del portador para solicitar un token de acceso. El token de acceso resultante refleja la identidad de la cuenta de servicio y puedes usarla para interactuar con las API de Google Cloud en nombre de la cuenta de servicio.

---

You are in charge of provisioning access for all Google Cloud users in your organization. Your
company recently acquired a startup company that has their own Google Cloud organization. You
need to ensure that your Site Reliability Engineers (SREs) have the same project permissions in the
startup company's organization as in your own organization. What should you do?

A. In the Google Cloud console for your organization, select Create role from selection, and choose
destination as the startup company's organization

B. In the Google Cloud console for the startup company, select Create role from selection and choose
source as the startup company's Google Cloud organization.

C. Use the gcloud iam roles copy command, and provide the Organization ID of the startup
company's

Google Cloud Organization as the destination.
D. Use the gcloud iam roles copy command, and provide the project IDs of all projects in the startup company s organization as the destination.
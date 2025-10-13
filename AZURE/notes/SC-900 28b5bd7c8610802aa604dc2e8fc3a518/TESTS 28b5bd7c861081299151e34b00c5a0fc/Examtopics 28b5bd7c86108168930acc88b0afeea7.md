# Examtopics

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image.png)

1. No
2. Yes
3. No

1. No - [https://azure.microsoft.com/en-us/pricing/details/active-directory/:](https://azure.microsoft.com/en-us/pricing/details/active-directory/:) Azure Active Directory comes in four editions—Free, Office 365 apps, Premium P1, and Premium P2.
2. Yes - [https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-access-create-new-tenant](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-access-create-new-tenant) You can do all of your administrative tasks using the Azure Active Directory (Azure AD) portal, including creating a new tenant for your organization.
3. No - [https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-whatis](https://docs.microsoft.com/en-us/azure/active-directory/fundamentals/active-directory-whatis) Azure Active Directory (Azure AD) is Microsoft’s cloud-based identity and access management service

---

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image%201.png)

[https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/](https://docs.microsoft.com/en-us/azure/cloud-adoption-framework/)
"The Cloud Adoption Framework is a collection of documentation, implementation guidance, best practices, and tools that are proven guidance from Microsoft designed to accelerate your cloud adoption journey."

---

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image%202.png)

Answer:eDiscovery

Digamos que customer LockBox sirve para que si el soporte tiene que solucionar algo en tu cloud donde tengas datos confidenciales estos te pediran permiso explicito por aquí.

eDiscovery se utiliza sobre todo para filtrar información que puedas necesitar de forma proactiva.

Customer Lockbox: This is a feature in cloud services that allows customers to have explicit control over when and how a cloud service provider can access their data. It's primarily a security and privacy feature.

Data Loss Prevention (DLP): DLP refers to a set of tools and processes used to prevent sensitive information from being accessed, shared, or distributed in an unauthorized manner.

Resource Lock: This is a term that might refer to a feature in cloud computing environments that allows users to prevent resources (such as virtual machines or storage) from being modified or deleted. It's a form of access control.

---

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image%203.png)

**Microsoft Intune** es un servicio de administración de puntos finales (endpoint management) unificado y basado en la nube que forma parte de la suite de seguridad y productividad de Microsoft. Su objetivo principal es ayudar a las organizaciones a **gestionar y proteger los dispositivos y aplicaciones** que sus empleados utilizan para acceder a los recursos corporativos.

- **Microsoft Endpoint Manager** es la plataforma unificada que Microsoft ofrece para gestionar y proteger los puntos finales (endpoints) en una organización. Esta plataforma **incluye Microsoft Intune** (para la gestión de dispositivos móviles y aplicaciones en la nube) y Configuration Manager (para la gestión de dispositivos en las instalaciones).
- El **Microsoft Endpoint Manager admin center** (también conocido como Microsoft Intune admin center) es el portal web centralizado desde donde se configuran y administran todas las funcionalidades de Intune, incluyendo el registro de dispositivos, la implementación de políticas de seguridad, la distribución de aplicaciones y la gestión de la conformidad de los dispositivos.
- **Azure Active Directory admin center (ahora Microsoft Entra admin center):** Se utiliza principalmente para gestionar identidades (usuarios, grupos, dispositivos registrados), acceso condicional y aplicaciones. Aunque Intune utiliza Microsoft Entra ID para la gestión de identidades, la administración específica de Intune no se realiza desde este portal.
- **Microsoft 365 compliance center (ahora Microsoft Purview compliance portal):** Se centra en la gestión de la conformidad y el riesgo, incluyendo eDiscovery, prevención de pérdida de datos (DLP), gestión de registros y auditoría. No se usa para administrar Intune.
- **Microsoft 365 Defender portal:** Es el centro de operaciones de seguridad para las soluciones de Microsoft Defender (Endpoint, Office 365, Identity, Cloud Apps). Se enfoca en la protección contra amenazas, la detección y respuesta a incidentes, no en la gestión de dispositivos y aplicaciones de Intune.

Es importante mencionar que Microsoft Intune es el componente principal basado en la nube de **Microsoft Endpoint Manager**. Microsoft Endpoint Manager es la solución unificada de Microsoft para la gestión de puntos finales, que combina las capacidades de Intune con las de Microsoft Configuration Manager (para entornos locales) para ofrecer una administración integral, ya sea totalmente en la nube, en las instalaciones o en un escenario híbrido (co-administración).

---

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image%204.png)

https://docs.microsoft.com/en-us/azure/active-directory/hybrid/whatis-fed

You can federate your on-premises environment with Microsoft Entra ID and use this federation for authentication and authorization. This sign-in method ensures that all user authentication occurs on-premises. This method allows administrators to implement more rigorous levels of access control. Federation with AD FS and PingFederate is available.

---

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image%205.png)

---

Which score measures an organization's progress in completing actions that help reduce risks associated to data protection and regulatory standards?

- A. Microsoft Secure Score
- B. Productivity Score
- C. Secure score in Azure Security Center
- D. Compliance score

Compliance = data protection regulations and industry standars

Microsoft Secure Score = Cybersecurity

Productivity Score = Microsoft 365 how people work.

Secure score in Azure Security cente = cibersecurity.

- **Compliance Score:** This score, found within **Microsoft Purview Compliance Manager**, specifically measures an organization's progress against data protection regulations and industry standards (like GDPR, HIPAA, ISO 27001, etc.). It provides actionable insights and tracks your journey towards compliance.

Let's look at why the others are incorrect:

- **A. Microsoft Secure Score:** This score, primarily associated with **Microsoft Defender XDR** (formerly Microsoft 365 Defender) and also seen in **Microsoft Defender for Cloud**, focuses on an organization's overall cybersecurity posture across various Microsoft products (endpoints, identity, email, cloud apps). While compliance can be a *driver* for some security actions, the Secure Score itself is broadly about reducing *cybersecurity risks*, not exclusively data protection and regulatory standards.
- **B. Productivity Score:** This score is part of **Microsoft 365** and measures how people work using Microsoft 365 services. It focuses on aspects like communication, collaboration, meetings, and content collaboration. It has nothing to do with security or compliance risks.
- **C. Secure score in Azure Security Center:** This is the *old name* for the **Secure Score in Microsoft Defender for Cloud**. As explained in option A, it measures general cybersecurity posture, not specifically data protection and regulatory standards.

---

What do you use to provide real-time integration between Azure Sentinel and another security source?

- A. Azure AD Connect
- B. a Log Analytics workspace
- C. Azure Information Protection
- D. a connector

"Built-in connectors enable connection to the broader security ecosystem for non-Microsoft products. For example, use Syslog, Common Event Format (CEF), or REST APIs to connect your data sources with Microsoft Sentinel.”

---

![image.png](Examtopics%2028b5bd7c86108168930acc88b0afeea7/image%206.png)

The Zero Trust model does not assume that everything behind the corporate firewall is safe, the Zero Trust model assumes breach and verifies each request as though it originated from an uncontrolled network.

Reference:

https://docs.microsoft.com/en-us/security/zero-trust/

---
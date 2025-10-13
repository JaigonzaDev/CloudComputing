# Cloud Build

**Cloud Build** es el servicio de **CI/CD (Integración Continua / Entrega Continua)** de **Google Cloud**. Te permite **compilar, testear y desplegar código automáticamente**, directamente desde repositorios como Cloud Source Repositories, GitHub o Bitbucket.

Cloud Build usa [Docker](https://docker.com/) para ejecutar compilaciones. Para cada paso de compilación, Cloud Build ejecuta un contenedor de Docker como una instancia de `docker run`. Actualmente, Cloud Build ejecuta la versión 20.10.24 del motor de Docker.

Es la automatización a nivel de software.

Digamos que tu puedes utilizar el código de cloud source repositories y compilarlo con Cloud build.
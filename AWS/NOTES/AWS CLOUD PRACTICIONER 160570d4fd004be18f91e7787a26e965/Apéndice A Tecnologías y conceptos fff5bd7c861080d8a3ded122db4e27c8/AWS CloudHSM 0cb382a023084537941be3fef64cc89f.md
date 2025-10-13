# AWS CloudHSM

¿Qué es?

**AWS CloudHSM (Hardware Security Module)** es un servicio de Amazon Web Services que proporciona módulos de seguridad de hardware (HSM) en la nube para la gestión de claves criptográficas y la protección de datos sensibles. A diferencia de los servicios de cifrado que operan solo a nivel de software, **CloudHSM** utiliza hardware especializado para realizar operaciones criptográficas, ofreciendo un nivel adicional de seguridad y cumplimiento.

¿Como funciona?

Básicamente es como un intermediario que hace que cuando pasas la información por ahí encripta la información y guarda las claves para que no esten expuestas y luego la devuelve encriptada. Luego para desencriptarla coge su llave asociada y la desencripta y te devuelve la información.
# Certificate error scenarios

Mientras navegamos, a veces encontramos **errores de certificados**. Estos indican posibles problemas con la seguridad. A continuación, se describen tres escenarios comunes:

### 1. Certificados autofirmados

Estos no están validados por una autoridad externa. A pesar de ser válidos, no son considerados de confianza.

- **Ejemplo**: Un navegador muestra una advertencia al acceder a un sitio con este tipo de certificado. El usuario decide si procede o no.

### 2. Certificados caducados

Son aquellos que han excedido su fecha de validez.

- **Ejemplo**: Al revisar un certificado, un símbolo (como un triángulo amarillo) señala que hay un problema, como una fecha de vencimiento pasada.

### 3. Revocación de certificados

Un certificado puede ser retirado por su autoridad certificadora.

- **Ejemplo**: Se usan tecnologías como CRL y OCSP para chequear la validez. Los navegadores tienen opciones para confirmar la validez consultando servidores OCSP.

**Consejo**: Siempre atiende los mensajes de error o advertencia en los navegadores. Comprender el mensaje ayuda a identificar y solucionar el problema.

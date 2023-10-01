## Resumen: Seguridad en Protocolos y Comunicaciones

### DNSSEC

**DNS** es un sistema que transforma nombres de dominio en direcciones IP. Por ejemplo, en lugar de recordar una dirección IP complicada, como `93.184.216.34`, simplemente recordamos `example.com`.

Pero el DNS tiene un problema: cualquiera en la red podría falsificar una respuesta DNS. Entonces, podrías terminar conectándote a un servidor malicioso sin saberlo. Aquí es donde entra **DNSSEC**:

- **Autenticidad**: Asegura que una respuesta DNS proviene del verdadero propietario del dominio.
- **Integridad**: Garantiza que la respuesta DNS no fue alterada en el camino.

### OpenPGP

Los correos electrónicos, originalmente, se enviaban como texto claro (similar a una postal abierta). Esto significa que cualquiera que interceptara el correo podía leerlo. A pesar de que ahora usamos protocolos seguros como `SMTPS`, `POP3S` y `IMAPS` que cifran los correos, los servidores de correo todavía pueden leer los mensajes.

**OpenPGP** es la solución:

- Es un estándar para cifrar y firmar correos electrónicos.
- Con OpenPGP, solo el destinatario previsto puede leer el correo.
- Ejemplo: Un mensaje simple "Hola, procede con la transacción" se convierte en un texto cifrado que parece aleatorio y es ilegible.

### SSH

Antiguamente, para administrar sistemas de forma remota, se usaban protocolos como **Telnet**. Pero estos protocolos enviaban todo en texto claro, incluidas las contraseñas.

**SSH** cambió todo eso:

- Proporciona una conexión cifrada, protegiendo la confidencialidad e integridad de los datos.
- A diferencia de Telnet, donde podías ver una contraseña como `RJ9wn^t3T%gC` en texto claro, con SSH todo es cifrado y seguro.

### Palabras clave:

- **DNSSEC**: Seguridad para respuestas DNS.
- **OpenPGP**: Cifrado de correos electrónicos.
- **SSH**: Conexiones seguras y cifradas para administración remota.

**Nota**: Es esencial mantener siempre actualizadas y protegidas nuestras herramientas y sistemas de seguridad. La seguridad en línea es una necesidad en el mundo actual.

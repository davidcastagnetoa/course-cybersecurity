# Protocolo SSL/TLS

**SSL (Secure Socket Shell)** y **TLS (Transport Layer Security)** son protocolos para cifrar datos entre un cliente (como un navegador) y un servidor. Piensa en TLS como una especie de "capa protectora" que convierte HTTP en HTTPS. Actualmente, TLS ha ido reemplazando a SSL.

## Funcionamiento de SSL/TLS:

¡Vamos a explicar el flujo de trabajo de SSL/TLS usando una analogía!

---

## La Carta Secreta 💌

1. **Saludo inicial (Handshake)**:

   - Antes de enviar la carta, llamas a tu amigo y le dices: "Hola, quiero enviarte una carta secreta". Tu amigo responde: "¡Genial, hagámoslo seguro!"

2. **Intercambio de códigos**:

   - Tú le dices a tu amigo que tienes una serie de códigos para cifrar la carta y le das algunas opciones. Tu amigo escoge uno que ambos conozcan.

3. **Verificación de identidad**:

   - Tu amigo te muestra una identificación (como un certificado) que ha sido firmada por alguien confiable (la Autoridad Certificadora).

4. **Creación de un secreto compartido**:

   - Ambos necesitan un "secreto compartido" para cifrar la carta. Imagina que es como un color especial de tinta invisible que ambos deben usar. Este color se crea combinando información de ambos, pero nunca se comparte directamente.

5. **Cifrado de la carta**:

   - Con ese "color especial de tinta invisible", escribes tu carta y la envías. Sólo tu amigo, usando el mismo color especial, puede leerla.

6. **Comunicación segura**:
   - Cada vez que quieras enviar una carta a tu amigo, la escribes con ese color especial. Así, aunque alguien intercepte la carta, no podrá leerla.

### RESUMEN

- **Saludo del Cliente**: Envía un mensaje al servidor con detalles técnicos.
- **Saludo del Servidor**: Responde al cliente con su certificado y otros detalles.
- **Autenticación**: El cliente verifica el certificado del servidor. Ejemplo: Al visitar Google, tu navegador verifica el certificado de Google.
- **Generación de Llaves**: El cliente y el servidor generan una llave de sesión, que nunca se transmite.
- **Mensajes de Listo**: Ambos indican que están listos para una conexión segura.

🔑 **Palabra clave**: Cifrado  
💡 **Ejemplo**: Es como un "apretón de manos" seguro antes de iniciar una conversación.

# Protocolo SOCKS5

**SOCKS (Socket Secure)** es un protocolo proxy para el intercambio de datos. Por ejemplo, el servidor Squid usa SOCKS5 para transferir datos vía HTTP.

## Funcionamiento de SOCKS5:

Imagina que SOCKS5 es como un intermediario en una conversación telefónica, donde una persona (Cliente A) quiere hablar con otra persona (Cliente B), pero no puede hacerlo directamente debido a ciertas restricciones. Así es cómo funciona SOCKS5:

1. **Llamada Inicial**:

   - Cliente A llama al intermediario (el proxy SOCKS5) y le dice: "Hola, soy Cliente A y quiero hablar con Cliente B".

2. **Respuesta del Intermediario**:

   - El intermediario (proxy SOCKS5) dice: "Muy bien, dime cómo prefieres que verifiquemos que eres realmente tú". En otras palabras, discuten cómo autenticarse.

3. **Autenticación**:

   - Cliente A le da al intermediario la información necesaria para verificar su identidad. Es como dar una contraseña o un código secreto.

4. **Petición de Conexión**:

   - Una vez autenticado, Cliente A le pide al intermediario que lo conecte con Cliente B. Le da al intermediario la "dirección" o detalles de Cliente B.

5. **Establecimiento de la Conexión**:

   - El intermediario establece la conexión con Cliente B y ahora, Cliente A y Cliente B pueden hablar entre ellos, pero todo lo que dicen pasa por el intermediario.

6. **Conversación**:
   - Cliente A y Cliente B intercambian mensajes o datos, pero en lugar de hacerlo directamente, lo hacen a través del intermediario (proxy SOCKS5).

### RESUMEN

- **Inicio del Cliente**: Cliente A se conecta con el proxy SOCKS5 y envía detalles específicos.
- **Respuesta del Proxy**: El proxy responde con un método de autenticación.
- **Transferencia de Datos**: Tras asociarse con el proxy, Cliente A y Cliente B pueden intercambiar datos a través del proxy.

🔑 **Palabra clave**: Proxy  
💡 **Ejemplo**: Imagina que SOCKS5 es como un intermediario que ayuda a dos personas a comunicarse a través de un muro.

## Beneficios de SOCKS5:

- Oculta detalles internos durante la comunicación.
- El proxy funciona como un relevo, permitiendo evitar la censura de Internet.

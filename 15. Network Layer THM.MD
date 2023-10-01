# Resumen: IPsec y VPN

## IPsec

**IPsec** es la abreviatura de "Internet Protocol Security". Se utiliza para añadir seguridad al tráfico de red mediante autenticación y protección de la integridad y confidencialidad de los datos.

### Puntos clave:

- **Authentication Header (AH):** Garantiza autenticación e integridad.
- **Encapsulating Security Payload (ESP):** Provee autenticación, integridad y cifrado.
- **Security Association (SA):** Negocia claves y algoritmos de cifrado.

## Authentication Header (AH)

**Authentication Header (AH)** es uno de los dos protocolos principales dentro de IPsec (el otro es ESP o Encapsulating Security Payload). AH fue diseñado con un propósito principal: **verificar la integridad y autenticidad de los datos** que se transmiten a través de una red. Sin embargo, es importante mencionar que AH **no cifra** los datos, por lo que no proporciona confidencialidad.

Para entenderlo mejor, considera AH como una especie de sello o firma que se añade a los datos. Este sello ayuda a garantizar que los datos no hayan sido modificados durante su tránsito y confirma que provienen de la fuente que dice ser.

## ¿Cómo funciona AH?

1. **Autenticación**: AH verifica que los datos no hayan sido alterados en tránsito. Es como recibir una carta con un sello que te asegura que nadie la ha abierto ni modificado desde que fue enviada.
2. **Integridad**: Asegura que los paquetes de datos no hayan sido alterados durante su tránsito. Si alguien intenta cambiar algún bit de información, el receptor se dará cuenta gracias a AH.

## Modos de operación de AH:

- **Modo Transporte**: En este modo, AH autentica solo la carga útil (datos) y la cabecera TCP/UDP. La cabecera IP original no se autentica. Es como si solo estuvieras asegurando el contenido de un sobre, pero no el sobre en sí.
- **Modo Túnel**: En este modo, se autentica toda la información, incluyendo la cabecera IP original. Es como si estuvieras asegurando tanto el contenido del sobre como el propio sobre.

**Nota**: Aunque AH puede ser útil en ciertos contextos, en muchas implementaciones modernas de IPsec, se prefiere usar ESP, ya que este último protocolo no solo autentica, sino que también cifra los datos, proporcionando así una mayor seguridad.

## Encapsulating Security Payload (ESP)

**ESP** es una sigla que significa _Encapsulating Security Payload_. Es un protocolo crucial dentro de **IPsec**, diseñado para ofrecer diversas medidas de seguridad para los paquetes de datos en una red.

### Características Principales:

1. **Cifrado de Datos:** ESP provee **confidencialidad** al cifrar los datos, asegurando que la información transmitida no pueda ser leída por personas no autorizadas, incluso si capturan los paquetes de datos.

2. **Autenticación:** Aunque su principal tarea es el cifrado, ESP también puede proporcionar **autenticación** de los datos, garantizando que los datos provienen de una fuente legítima.

3. **Integridad:** ESP asegura la **integridad** de los datos, verificando que los datos no hayan sido alterados durante su tránsito.

### Modos de Operación:

- **Modo Transporte:** En este modo, ESP protege únicamente el contenido de los paquetes (carga útil), pero no la cabecera. Es comúnmente utilizado cuando la comunicación es entre dos hosts finales.

- **Modo Túnel:** En este modo, ESP protege tanto la carga útil del paquete como la cabecera. Esto es útil cuando, por ejemplo, se conecta un usuario a una red privada a través de una VPN. En este escenario, el paquete entero es cifrado y luego encapsulado dentro de un nuevo paquete IP.

En resumen, ESP es esencial para mantener la seguridad y privacidad de los datos transmitidos en redes que utilizan IPsec, ya sea para comunicaciones punto a punto o para conexiones VPN.

### Ejemplos:

- **AH en Modo de Transporte:** Autentica la cabecera y datos de TCP/UDP.
- **ESP en Modo de Túnel:** Protege y cifra la cabecera IP, cabecera TCP/UDP y datos.

---

## VPN (Red Privada Virtual)

**VPN** permite establecer conexiones privadas a través de redes públicas. Es decir, puedes tener una conexión segura utilizando una infraestructura no segura.

### Palabras clave:

- **IPsec y SSL/TLS:** Protocolos comunes para establecer conexiones VPN.
- **PPTP:** Protocolo antiguo que ya no se considera seguro.

### Ejemplos:

Imagina una oficina remota y un usuario remoto que se conectan al edificio principal de una empresa a través de una **VPN**. Todo el tráfico entre ellos está cifrado, como si estuvieran conectados directamente por un cable privado, aunque en realidad utilizan la infraestructura del internet público.

---

### Puntos Importantes:

1. **IPsec** protege el tráfico de red mediante autenticación y cifrado.
2. **VPN** permite conectar redes o usuarios de manera segura sobre el internet público.
3. Aunque **SSL** fue creado para el tráfico HTTP, también se usa para conexiones VPN seguras con herramientas como **OpenVPN**.
4. No todos los protocolos VPN son seguros; por ejemplo, **PPTP** ya no es recomendable.

---

### Preguntas y Respuestas:

- **¿Qué protocolo utiliza el cliente VPN de Cisco para establecer una conexión VPN?**  
  **Respuesta:** El cliente VPN de Cisco utiliza **IPsec** para establecer conexiones VPN.

- **¿Qué protocolo utiliza el proyecto OpenVPN para cifrado y autenticación?**  
  **Respuesta:** OpenVPN utiliza **SSL/TLS** para cifrado y autenticación.

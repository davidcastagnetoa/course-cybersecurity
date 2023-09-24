# RADIUS y TACACS+ Explicados

## Resumen:

### 1. **RADIUS**:

- Sistema compuesto por el **suplicante**, **cliente RADIUS** y **servidor RADIUS**.
- Autenticación a través de certificados, nombres de usuario, contraseñas o tokens RSA.
- Opera sobre **UDP** en puertos 1812, 1813, 1645 o 1646.
- Común en redes inalámbricas.

### 2. **TACACS+**:

- Protocolo desarrollado por **Cisco** para administrar el acceso a enrutadores y conmutadores.
- Menos común en redes inalámbricas.
- Comprende el **servidor TACACS+** y el **cliente TACACS+**.
- Funciona sobre **TCP** y utiliza el puerto 49.

Ambos protocolos son **AAA**, proporcionando autenticación, autorización y contabilidad.

**Palabras clave**:

- RADIUS
- TACACS+
- AAA
- Autenticación
- Autorización
- Contabilidad
- UDP
- TCP

## INTRODUCCION

---

## RADIUS (Remote Authentication Dial-In User Service):

**Descripción:** RADIUS es como un portero que verifica quién puede entrar a un club exclusivo.

### Componentes Principales:

1. **Suplicante:** Es la persona (o dispositivo) que quiere entrar al "club" y necesita ser verificada.
2. **Cliente RADIUS:** Es el encargado de recibir las solicitudes del suplicante y enviarlas al jefe (servidor RADIUS) para ver si tiene permiso para entrar.
3. **Servidor RADIUS:** Es el "jefe" que tiene la lista de quién puede y quién no puede entrar. Decide si el suplicante tiene permiso basándose en ciertas credenciales.

### Funcionamiento:

- Cuando alguien quiere conectarse a una red (como una red Wi-Fi), el dispositivo envía una solicitud al cliente RADIUS. Este cliente luego le pregunta al servidor RADIUS si esa persona tiene permiso.
- El servidor RADIUS verifica las credenciales (como nombres de usuario y contraseñas) y responde con un sí o no.
- RADIUS opera sobre el protocolo UDP, un tipo de protocolo de internet.

---

## TACACS+ (Terminal Access Controller Access-Control System Plus):

**Descripción:** TACACS+ es similar a RADIUS pero está diseñado especialmente para empresas con muchos enrutadores y conmutadores. Es como tener un sistema de seguridad especial para los empleados que gestionan las redes.

### Componentes Principales:

1. **Cliente TACACS+:** Representa los enrutadores y conmutadores en una empresa. Cuando un administrador quiere acceder a uno de estos enrutadores, el cliente TACACS+ verifica si tiene permiso.
2. **Servidor TACACS+:** Es el que decide si el administrador tiene permiso para acceder a los enrutadores y conmutadores.

### Funcionamiento:

- Fue creado por Cisco porque en empresas grandes con muchos enrutadores y conmutadores, era un lío que los administradores tuvieran que ingresar a cada uno por separado.
- TACACS+ verifica a los administradores y les da permiso para gestionar la red.
- Opera sobre el protocolo TCP, otro tipo de protocolo de internet.

---

**Conclusión:** Ambos, RADIUS y TACACS+, son sistemas que ayudan a las organizaciones a controlar quién tiene acceso a sus redes y recursos. La diferencia principal es su enfoque y cómo operan. Es como tener dos diferentes tipos de sistemas de seguridad: uno para los invitados regulares y otro para el equipo de seguridad interno.

# Resumen de Protocolos de Seguridad

## 🌐 **HTTPS**

- **Concepto:** Versión segura de HTTP. Permite comunicación cifrada entre un navegador y un servidor web.
- **Uso:** Seguro para transacciones, como compras en línea o banca en línea.
- **Ejemplo:** Cuando ves un candado en tu navegador, estás usando HTTPS.

## 📂 **FTPS**

- **Concepto:** FTP pero con seguridad añadida. Transfiere archivos de manera cifrada.
- **Diferencia Principal:** FTP envía datos en texto claro; FTPS los cifra.
- **Ejemplo:** Usar un programa como Filezilla para transferir archivos, pero de forma segura.

## 💌 **SMTPS**

- **Concepto:** SMTP (protocolo para enviar correos) pero seguro.
- **Uso:** Asegura que los correos se envíen de forma cifrada.
- **Ejemplo:** Cuando envías un correo desde tu aplicación favorita, y este se envía cifrado.

## 📬 **POP3S**

- **Concepto:** POP3 (protocolo para descargar correos) pero seguro.
- **Limitaciones de POP3:** Descarga emails en un dispositivo y los borra del servidor. Además, transmite en texto claro.
- **Ejemplo:** Cuando descargas correos en tu computadora, y estos se descargan cifrados.

## 📌 **Puntos Clave**

- La mayoría de los protocolos seguros añaden una capa de cifrado, como TLS/SSL.
- Es esencial usar versiones seguras de protocolos, especialmente al manejar datos sensibles.

---

## Puertos Determinados para Protocolos

### 1. HTTPS Protocol

- **Puerto:** 443

### 2. HTTP Protocol

- **Puerto:** 80

  _Ejemplo:_ Cuando ingresas a un sitio web usando "http://", estás usando el puerto 80.

### 3. FTPS Protocol

- **Puerto estándar de FTP y FTPS explícito:** 21
- **Puerto para FTPS implícito:** 990

  _Ejemplo:_ Al transferir archivos a un servidor usando FTPS, podrías estar utilizando el puerto 990 para una conexión segura.

### 4. SMTPS Protocol

- **Puertos comunes:** 587 y 465

  _Ejemplo:_ Al enviar un correo electrónico de forma segura, es probable que tu cliente de correo utilice uno de estos puertos.

### 5. POP3 Protocol

- **Puerto:** 110
- **Puerto para POP3S (versión segura):** 995

  _Ejemplo:_ Al recibir correos electrónicos en un programa como Outlook o Thunderbird, se podría usar el puerto 995 para una conexión segura con POP3S.

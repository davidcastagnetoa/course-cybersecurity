# Kerberos y EAP: Una Introducción

## Explicación Detallada y Simple:

**Kerberos** y **EAP** son protocolos de autenticación. Mientras que Kerberos está diseñado principalmente para redes de área local cableadas (como las que usamos en nuestras oficinas o hogares), EAP es más flexible y se usa a menudo para la autenticación en redes inalámbricas.

Kerberos trabaja con un concepto llamado "token", que es un comprobante de autenticidad. Cuando tu computadora quiere acceder a recursos en una red, envía información al servidor Kerberos, que verifica esta información y envía un token de vuelta. Esto permite que tu computadora pruebe quién dice ser.

Por otro lado, **EAP** (Extensible Authentication Protocol) es como un sobre que contiene información sobre cómo debe realizarse la autenticación. Hay diferentes versiones de EAP, algunas usan claves, otras contraseñas y otras certificados. EAP es como un lenguaje común que permite que diferentes dispositivos y sistemas se entiendan entre sí cuando se trata de autenticación.

## Resumen:

**Kerberos** es un protocolo de autenticación diseñado para redes cableadas que utiliza tokens. **EAP** es un protocolo más flexible que actúa como un "sobre", definiendo cómo se debe llevar a cabo la autenticación, siendo comúnmente utilizado en redes inalámbricas.

## Palabras clave:

- Kerberos
- EAP (Extensible Authentication Protocol)
- Autenticación
- Token
- Red cableada
- Red inalámbrica
- Certificados
- Contraseñas

## Token: Explicación Simple

Imagina que vas a un club nocturno y, al entrar, el portero te da una pulsera especial. Esa pulsera es tu "token" que te permite entrar y salir del club durante toda la noche. Si algún otro portero te ve sin la pulsera, sabrá que no has sido autenticado y no te permitirá entrar. Sin embargo, si la tienes, te dejará pasar sin problemas porque ya fuiste verificado anteriormente.

De manera similar, en el mundo digital, un **token** es como esa pulsera especial. Es un comprobante electrónico que demuestra que ya te has identificado ante un sistema o aplicación. Por lo general, después de ingresar tu nombre de usuario y contraseña, el sistema te da un token que tu dispositivo guarda. Así, las próximas veces que intentes acceder, el sistema simplemente revisará el token en lugar de pedirte nuevamente las credenciales. Esto hace que el acceso a aplicaciones y servicios sea más rápido y seguro.

Además, los tokens tienen otras ventajas:

- **Seguridad**: A menudo están diseñados para ser temporales, lo que significa que caducan después de un tiempo. Así que, aunque alguien robe tu token, no podrá usarlo indefinidamente.
- **Privacidad**: A diferencia de las contraseñas, los tokens no revelan información sobre tu identidad real, solo demuestran que tienes permiso para hacer algo.

En resumen, un **token** es como una pulsera electrónica que te da permiso para acceder a ciertos lugares o servicios en línea. Es una forma eficiente y segura de probar quién eres sin tener que ingresar tu contraseña todo el tiempo.

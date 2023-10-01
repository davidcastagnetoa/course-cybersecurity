# Explicación y Resumen del Texto

## Explicación Detallada

Compartir carpetas en grupos de trabajo proviene de una antigua función de red de más de 30 años. Originariamente, Microsoft compartía información a través de una función llamada NetBIOS/NetBEUI. Aquí, NetBIOS era el sistema de nomenclatura (limitado a solo 15 caracteres), mientras que NetBEUI creaba las conexiones entre los sistemas. Sin embargo, esto no usaba TCP/IP, era exclusivamente para redes locales pequeñas.

A medida que TCP/IP se popularizaba, Microsoft introdujo NetBT, que significa NetBIOS sobre TCP/IP. Este sistema desechó el antiguo NetBEUI y adoptó direcciones IP, pero conservó la misma nomenclatura.

Posteriormente, Microsoft quería que las personas pudieran compartir carpetas en Internet de la misma manera que en una oficina. Introdujeron CIFS (sistema de archivos común de Internet) y más tarde SMB (bloques de mensajes del servidor). Hoy en día, otros sistemas operativos también utilizan SMB bajo nombres como Samba.

La demostración en el texto muestra dos computadoras, una con Windows 7 y otra con Windows 10, ambas en el mismo grupo de trabajo. En una red Windows, simplemente pon todos en la misma red local y con el mismo nombre de grupo de trabajo, y comenzarán a detectarse automáticamente. Sin embargo, cuando intentamos acceder a un recurso compartido en una máquina desde otra, podríamos enfrentar problemas de permisos si los usuarios no coinciden o tienen diferentes contraseñas en las máquinas.

Es crucial entender que cada sistema tiene sus propias cuentas. Por ejemplo, la cuenta "Mike" en un sistema Windows 7 no es la misma que la cuenta "Mike" en Windows 10, incluso si tienen el mismo nombre.

En entornos domésticos, para facilitar el acceso, a menudo se configuran las mismas cuentas con las mismas contraseñas en todos los sistemas. Sin embargo, esta práctica es insegura en entornos empresariales. Las soluciones empresariales prefieren usar logins de dominio del directorio activo.

## Resumen

Cuando hablamos de compartir carpetas en grupos de trabajo, estamos tratando con sistemas que datan de hace 30 años, como NetBIOS/NetBEUI. Estos sistemas evolucionaron con el tiempo, adaptándose a las necesidades de las redes modernas, dando paso a protocolos como NetBT y SMB. Aunque parece sencillo compartir archivos entre máquinas en la misma red, existen desafíos con respecto a los permisos y las cuentas de usuario. Mientras que tener el mismo nombre de usuario y contraseña en todas las máquinas puede funcionar en casa, es una práctica insegura en empresas, donde se prefiere usar directorios activos.

## Palabras Clave

- NetBIOS/NetBEUI
- NetBT
- SMB
- Grupos de trabajo
- CIFS
- Samba

## Puntos Importantes

1. NetBIOS/NetBEUI son sistemas antiguos para compartir recursos.
2. SMB es el protocolo moderno para compartir recursos.
3. Las cuentas de usuario en diferentes máquinas, aunque tengan el mismo nombre, no son las mismas.
4. En entornos empresariales, es preferible usar directorios activos en lugar de grupos de trabajo debido a problemas de seguridad.

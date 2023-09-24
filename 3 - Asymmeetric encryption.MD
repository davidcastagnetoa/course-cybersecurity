## Resumen sobre Cifrado Asimétrico

El cifrado simétrico presenta el desafío de que ambas partes deben tener una copia de la clave para descifrar datos. Esta transmisión de claves puede ser vulnerable. Para solucionar este problema, Rivest, Shamir y Adleman propusieron el cifrado asimétrico.

En este enfoque, no hay una única clave; en su lugar, hay dos: una clave pública y una clave privada.

La clave pública sólo cifra datos, mientras que la clave privada se utiliza para descifrar. Por ejemplo, si Mike Meyers desea enviar un mensaje cifrado a Mike Jones, emplearía la clave pública de Jones para cifrarlo. Jones, a su vez, usaría su clave privada para descifrar el mensaje.

Las claves públicas se pueden compartir abiertamente, pero las claves privadas deben protegerse y mantenerse en secreto. Por lo general, uno tendrá múltiples claves públicas de diferentes personas almacenadas para uso futuro.

### Palabras clave:

- **Cifrado simétrico**
- **Cifrado asimétrico**
- **Rivest, Shamir, Adleman**
- **Clave pública**
- **Clave privada**
- **Intercambio de claves**
- **Cifrar**
- **Descifrar**

# Hashes Criptográficos

En la **seguridad de datos**, más allá del cifrado, a veces lo que se busca es simplemente **verificar** la integridad de los datos. Esta verificación se realiza utilizando un proceso llamado **"hashing"**.

Un hash es un algoritmo que no cifra, sino que convierte cualquier cantidad de datos en un valor de tamaño fijo, como 128 bits.

La magia del hash radica en que **cualquier pequeño cambio** en los datos originales (incluso cambiar una sola letra) resulta en un **valor de hash completamente diferente**.

Los hashes son útiles para confirmar que los datos no han sido alterados de ninguna manera. Por ejemplo, cuando se descarga un archivo grande como una distribución de Linux, se puede **proporcionar** un valor hash para que los usuarios puedan **verificar** que su descarga no se ha corrompido o modificado.

Existen diferentes tipos de algoritmos de hash, siendo **MD5** y **SHA-1** los más comunes, pero también existe **SHA-2**, que tiene variantes como SHA-256 y SHA-384.

El hashing no es un método de cifrado ni de autenticación; es simplemente una forma de **verificar la integridad de los datos**.

### Palabras Clave

- **Hashing**
- **Cifrado**
- **Integridad de datos**
- **MD5**
- **SHA-1**
- **SHA-2**
- **Verificación**
- **Algoritmo**
- **Valor de tamaño fijo**
- **Descarga**

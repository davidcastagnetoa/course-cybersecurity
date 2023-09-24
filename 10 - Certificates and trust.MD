# Certificates and trust

Uno de los grandes desafíos para usar el cifrado asimétrico es garantizar que la clave pública que crees que pertenece a alguien realmente le pertenezca.

## Generación de claves

Uno de los grandes desafíos para usar el cifrado asimétrico es asegurarse de que las personas estén utilizando las claves correctas.

### Servidor Web Ejemplo

Digamos que soy un servidor web y soy dueño de una compañía que vende zapatos online. Si quieres conectarte a mi sitio y comprar zapatos, necesitarás obtener mi clave pública para poder cifrar la información que me envías.

## Problemas con cifrado asimétrico

El problema con el cifrado asimétrico es que, si bien es súper seguro, es increíblemente lento. Por tanto, no es práctico cifrar grandes cantidades de información con él.

### Clave Pública vs Clave Privada

Recuerde que hemos dicho en episodios anteriores que tienes una clave pública, que es conocida por todos, y una clave privada que es secreta.

### Firma Digital

Entonces, lo que haremos es no simplemente enviar la clave pública por sí sola, sino enviarla junto con una firma digital.

### Certificado Digital

Lo que hacemos en su lugar es generar algo llamado certificado digital. Un certificado digital es básicamente una clave pública junto con alguna información adicional, y todo eso es firmado por una entidad confiable.

#### Envío de certificados

Puedo tomar el certificado y ponerlo en mi servidor web, y cuando te conectes a mi sitio, te enviaré el certificado.

### Confianza en Certificados

El truco aquí es ¿en quién confías? Bueno, para eso hay varias formas.

#### Certificado sin Firmar

La primera forma de confiar es generar un certificado por su cuenta. Esta es la forma menos confiable de confiar en un certificado, porque no hay una tercera parte que verifique que es legítimo.

#### Red de Confianza

Aparte de eso, tiene otras dos opciones, web de confianza y PKI. La web de confianza es básicamente decir: "Confío en esta persona y si esa persona confía en otra persona, entonces también confiaré en esa otra persona".

##### Crecimiento de Red de Confianza

Y ahora esta red de confianza puede crecer. Si confío en cinco personas y esas cinco personas confían en otras cinco personas, entonces hay 25 personas en mi red de confianza.

### Infraestructura de Clave Pública

Si realmente desea confiar en los certificados de la manera correcta, necesita una Infraestructura de Clave Pública o PKI.

En resumen, el cifrado asimétrico es poderoso, pero para que funcione correctamente en la web, es esencial gestionar y confiar en las claves de forma adecuada. Las firmas digitales, los certificados y _las autoridades de certificación (CA)_ son herramientas esenciales para establecer esa confianza.

# Administrar usuarios en AD

Como **nuevo administrador del dominio**, debes:

1. **Revisar y eliminar** las OUs no necesarias en AD. Desactiva la protección contra eliminaciones accidentales para hacerlo.
2. **Ajustar los usuarios** de AD según el organigrama empresarial.
3. Utilizar la **delegación** en AD para otorgar a ciertos usuarios, como Phillip, control sobre OUs específicos.
4. **Restablecer contraseñas** con Powershell usando las credenciales de Phillip.
5. **Forzar cambios de contraseña** en el próximo inicio de sesión.
6. **Iniciar sesión** con el usuario afectado, en este caso, Sophie, para comprobar los cambios.

## Organigrama

![Managing Users in Active Directory](/images/ManagingUsersinAD01.png)

## Problema con la Unidad Organizativa en AD

En AD, hay una **unidad organizativa de departamento** que no coincide con el gráfico. Esta unidad, cerrada por **recortes presupuestarios**, al intentar ser eliminada, arroja un **error**.

![Managing Users in Active Directory](/images/ManagingUsersinAD02.png)

## Eliminación de OUs en AD

Las OUs están **protegidas por defecto** contra eliminación accidental. Para eliminarlas, es necesario activar las **Funciones Avanzadas** en el menú **Ver**.

![Managing Users in Active Directory](/images/ManagingUsersinAD03.png)

## Desactivación de Protección y Ajustes en AD

- Accede a **contenedores adicionales** y desactiva la protección contra **eliminación accidental** en la OU.
- Al intentar **eliminar la OU**, confirma la acción. Ten en cuenta que esto afectará a todos los elementos asociados.
- Verifica que los **usuarios en AD** coincidan con el gráfico organizacional y realiza los ajustes pertinentes.

![Managing Users in Active Directory](/images/ManagingUsersinAD04.png)

## Delegación en AD

En AD, se puede otorgar a usuarios específicos control sobre ciertas **Unidades Organizativas (OUs)** a través de un proceso llamado **delegación**. Esto permite asignar privilegios específicos sin necesidad de un Administrador del Dominio.

Un ejemplo práctico es brindar al soporte de TI, en este caso **Phillip**, el poder de restablecer contraseñas en las OUs de Ventas, Marketing y Gestión.

![Managing Users in Active Directory](/images/ManagingUsersinAD05.png)

## Delegación de Control en Windows

Al tratar de delegar control, se mostrará una ventana pidiendo seleccionar los usuarios a los que se desea otorgar dicho control.

**Nota:** Para evitar errores al escribir, simplemente ingresa "phillip" y haz clic en "Check Names". Windows completará el nombre del usuario por ti.

![Managing Users in Active Directory](/images/ManagingUsersinAD06.png)
![Managing Users in Active Directory](/images/ManagingUsersinAD07.png)

## Delegación de Restablecimiento de Contraseñas

Una vez se haya avanzado seleccionando "next" varias veces, Phillip adquiere la habilidad de cambiar contraseñas para cualquier miembro del departamento de ventas. Es recomendable repetir este proceso para los departamentos de Marketing y Administración, pero dejaremos ese paso a discreción. Se puede continuar con la configuración de otras unidades organizativas si se prefiere.

## Restablecimiento de Contraseña con la Cuenta de Phillip

Para intentar cambiar la contraseña de Sophie, utiliza las siguientes credenciales de Phillip:

- **Usuario:** phillip
- **Contraseña:** Claire2008

## Instrucciones para el Restablecimiento de Contraseña

1. Al conectar vía RDP, ingresa con el nombre de usuario `THM\phillip` para acceder como phillip en el dominio THM.
2. No intentes abrir "Active Directory Users and Computers" con Phillip ya que no tiene los privilegios necesarios.
3. Utiliza el siguiente comando en Powershell para restablecer la contraseña:

```powershell
PS C:\Users\phillip> Set-ADAccountPassword sophie -Reset -NewPassword (Read-Host -AsSecureString -Prompt 'New Password') -Verbose
```

Deberias observar lo siguiente tras restablecer la contraseña:

```powershel
VERBOSE: Performing the operation "Set-ADAccountPassword" on target "CN=Sophie,OU=Sales,OU=THM,DC=thm,DC=local".
```

## Forzar Cambio de Contraseña en el Próximo Inicio de Sesión

Para asegurarnos de que Sophie cambie su contraseña en su próximo inicio de sesión, utiliza el siguiente comando en Powershell:

```powershell
PS C:\Users\phillip> Set-ADUser -ChangePasswordAtLogon $true -Identity sophie -Verbose
```

Deberias observar lo siguiente una vez ejecutado el comando :

```powershell
 VERBOSE: Performing the operation "Set" on target "CN=Sophie,OU=Sales,OU=THM,DC=thm,DC=local".
```

## Acceso a la Cuenta de Sophie

Finalmente, inicia sesión en la cuenta de Sophie con la contraseña recién establecida. Tu objetivo es recuperar una bandera del escritorio de Sophie.

**Nota:** Al conectarte a través de RDP, utiliza `THM\sophie` como nombre de usuario para especificar que deseas ingresar como Sophie en el dominio THM.

> Este paso final te permitirá verificar que tienes acceso a la cuenta de Sophie y recuperar la información requerida.

<!-- https://youtu.be/dwP4jpXdSp4?si=Z2dE6lvJtpSFfWFs&t=2053 -->

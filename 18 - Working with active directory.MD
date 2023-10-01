# Explicación detallada sobre el trabajo con Active Directory

**Active Directory (AD)** es un sistema de administración de identidad y acceso de Microsoft utilizado principalmente en entornos de red corporativos para centralizar y administrar la información y los recursos.

## Cambio de grupos de trabajo a dominios AD

- **Dominio y Controladores de Dominio:** Cambiar de un grupo de trabajo a un dominio AD requiere un controlador de dominio, esencialmente una computadora dedicada con Windows Server. Este controlador podría tener múltiples funciones, como servir archivos.
- **Cuentas:** En un grupo de trabajo, cada computadora mantiene sus propias cuentas locales. Con AD, usamos cuentas de dominio centralizadas.

- **Seguridad y organización:** AD proporciona más opciones de seguridad y organización. Las cuentas pueden organizarse en **Unidades Organizativas (OUs)** para una mejor estructuración. Además, se pueden aplicar políticas de seguridad a nivel de dominio.
- **Nombres de dominio:** En AD, en lugar de simplemente un nombre de computadora, usamos nombres de dominio, que pueden ser completos (por ejemplo, `TotalSeminars.com`) o específicos de la intranet (por ejemplo, `name.local`).

- **Herramientas Administrativas:** AD viene con herramientas especiales para administrar usuarios, grupos y recursos, como "Active Directory Users and Computers".
- **Potencia de las cuentas de dominio:** Un administrador de dominio tiene poder sobre todo el dominio y puede hacer casi cualquier cosa. Es más potente que un administrador local.

- **Características adicionales:** AD permite configurar horas de inicio de sesión, carpetas de inicio, scripts de inicio de sesión y mucho más.

## Resumen con Ejemplo:

Imagina que tu empresa es una ciudad (dominio). Antes, cada edificio (computadora) en esa ciudad tenía sus propias reglas y listas de residentes (cuentas locales). Ahora, con Active Directory, hay un ayuntamiento (Controlador de Dominio) que tiene una lista central de todos los residentes y reglas para toda la ciudad. Así que si un residente (cuenta de dominio) quiere entrar en cualquier edificio, solo necesita su identificación del ayuntamiento, en lugar de una para cada edificio.

---

**Palabras clave:** Active Directory, Controlador de Dominio, Cuentas de Dominio, Grupos de Trabajo, Políticas de Seguridad, Unidades Organizativas, Herramientas Administrativas.

## Puntos clave:

- Cambiar a un dominio AD implica usar un Controlador de Dominio.
- Las cuentas de dominio reemplazan a las cuentas locales en AD.
- Active Directory ofrece potentes herramientas y opciones de seguridad.
- Un administrador de dominio tiene poderes amplios en el dominio.

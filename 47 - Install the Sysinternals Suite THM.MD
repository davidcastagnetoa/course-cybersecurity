# Trabajando con Sysinternals

## Explicación Detallada y Amplia

Las **Herramientas Sysinternals** ofrecen una amplia gama de utilidades para sistemas Windows, disponibles para descarga o ejecución directa desde la web.

### Instalación y Ejecución Local

Puedes descargar toda la suite de Sysinternals o herramientas individuales según tus necesidades:

- **Descarga Individual:** Si solo necesitas una o dos herramientas, visita la página de Índice de Utilidades de Sysinternals [aquí](https://docs.microsoft.com/en-us/sysinternals/downloads/). Las herramientas están listadas en orden alfabético y no están separadas por categorías. Esto es útil si sabes exactamente qué herramientas necesitas.

  ![Screenshot mostrando la página del Índice de Utilidades de Sysinternals](/images/InstallSysinternalsSuite001.png)

- **Descarga por Categorías:** Si estás interesado en herramientas específicas dentro de una categoría, por ejemplo, Utilidades de Proceso, puedes ir a la página correspondiente como [esta](https://docs.microsoft.com/en-us/sysinternals/downloads/process-utilities/). Aquí encontrarás todas las herramientas relacionadas con esa categoría.

  ![Screenshot mostrando la página de Utilidades de Proceso de Sysinternals](/images/InstallSysinternalsSuite002.png)

- **Suite de Sysinternals:** Para una colección más completa, puedes descargar la suite completa desde [este enlace](https://learn.microsoft.com/en-us/sysinternals/downloads/sysinternals-suite). Después de descargar el archivo zip, debes extraer los archivos. Opcionalmente, puedes agregar la ruta del directorio de la suite a las variables de entorno para ejecutar las herramientas desde la línea de comandos sin tener que navegar al directorio.

  ![Screenshot mostrando las herramientas incluidas en la Suite de Sysinternals](/images/InstallSysinternalsSuite004.png)

### Ejecución desde la Web

- **Sysinternals Live URL:** Accede a [https://live.sysinternals.com/](https://live.sysinternals.com/) para ejecutar herramientas directamente desde la web. Este método es útil si prefieres no descargar las herramientas.

  ![Screenshot mostrando la página de live.sysinternals.com](/images/InstallSysinternalsSuite003.png)

### Configuración de Variables de Entorno

Si descargas la suite, considera agregar la ruta del directorio a las variables de entorno para facilitar el acceso a las herramientas:

1. Ejecuta `sysdm.cpl` desde la línea de comandos para abrir Propiedades del Sistema.
2. En la pestaña Avanzado, selecciona 'Variables de Sistema'.
3. Agrega la ruta del directorio donde extrajiste la suite de Sysinternals.

![Screenshot mostrando la pestaña Avanzada de Propiedades del Sistema](/images/InstallSysinternalsSuite005.png)
![Screenshot mostrando la pestaña Avanzada de Propiedades del Sistema](/images/InstallSysinternalsSuite006.png)
![Screenshot mostrando la pestaña Avanzada de Propiedades del Sistema](/images/InstallSysinternalsSuite007.png)

### Uso de PowerShell

Alternativamente, puedes utilizar un módulo de PowerShell para descargar e instalar todas las herramientas de Sysinternals:

```powershell
Download-SysInternalsTools C:\Tools\Sysint
```

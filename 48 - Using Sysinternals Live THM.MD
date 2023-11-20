# Uso de Sysinternals Live

## Explicación Detallada y Amplia

Sysinternals Live es un servicio que permite ejecutar herramientas Sysinternals directamente desde la web, facilitando el acceso sin necesidad de descargarlas manualmente.

### Ejecución de Herramientas Sysinternals desde la Web

Para lanzar una herramienta Sysinternals desde la web, se utiliza la sintaxis `\\live.sysinternals.com\tools\<nombre_herramienta>`. Por ejemplo, para ejecutar Process Monitor, el comando sería `\\live.sysinternals.com\tools\procmon.exe`.

#### Problemas y Soluciones

- **Error de Ejecución:** Si al intentar ejecutar la herramienta aparece el error "No se puede encontrar la ruta especificada", esto se debe a que el cliente WebDAV no está instalado o en funcionamiento.

  ![Captura de pantalla mostrando el error](/images/UsingSysinternalsLive001.png)

- **Cliente WebDAV:** El protocolo WebDAV permite que una máquina local acceda a una remota que comparte archivos mediante WebDAV. En Windows 10, el cliente está instalado pero probablemente no esté en funcionamiento.

  ![Captura de pantalla mostrando los pasos para iniciar el servicio webclient](/images/UsingSysinternalsLive012.png)

- **Inicio del Servicio WebClient:** Antes de intentar llamar a cualquier herramienta Sysinternals de esta manera, el servicio WebClient debe estar en funcionamiento.

  ![Captura de pantalla mostrando el comando para verificar el servicio webclient](/images/UsingSysinternalsLive003.png)

- **Habilitar Descubrimiento de Red:** También es necesario habilitar el Descubrimiento de Red, lo cual se puede hacer en el Centro de redes y recursos compartidos.

  ![Captura de pantalla del comando para abrir el Centro de redes y recursos compartidos](/images/UsingSysinternalsLive005.png)

### En Windows Server 2019

- **Instalación de WebDAV Redirector:** En Windows Server 2019, el cliente WebDAV no viene instalado por defecto. Se puede instalar con PowerShell usando el comando `Install-WindowsFeature WebDAV-Redirector –Restart`.

  ![Captura de pantalla verificando la instalación de WebDAV Redirector](/images/UsingSysinternalsLive014.png)

### Métodos de Ejecución

1. **Desde la Línea de Comandos:** Ejecuta la herramienta directamente desde la línea de comandos.

   ![Captura de pantalla de una herramienta de Sysinternals iniciada desde la línea de comandos](/images/UsingSysinternalsLive007.png)

2. **Desde una Unidad de Red Mapeada:** Crea una unidad de red y ejecuta la herramienta desde la unidad mapeada.

   ![Captura de pantalla mostrando cómo se conecta la unidad Y a live.sysinternals.com\tools](/images/UsingSysinternalsLive008.png)

   **Nota:** El asterisco asignará automáticamente una letra de unidad. También puedes especificar una letra de unidad manualmente.

   ![Captura de pantalla mostrando la unidad Y entre las ubicaciones de red](/images/UsingSysinternalsLive009.png)

   Ahora, el sitio web es navegable desde la máquina local.

   ![Captura de pantalla navegando por la unidad Y desde el símbolo del sistema](/images/UsingSysinternalsLive010.png)
   ![Captura de pantalla mostrando la página de ayuda lanzada desde el símbolo del sistema para la herramienta Process Monitor](/images/UsingSysinternalsLive011.png)

## Resumen

- **Sysinternals Live:** Permite ejecutar herramientas directamente desde la web.
- **Cliente WebDAV y Descubrimiento de Red:** Requisitos para la ejecución exitosa.
- **Métodos de Ejecución:** Desde la línea de comandos o unidad de red mapeada.

## Puntos Clave

- **Facilidad de Acceso:** Ejecuta herramientas Sysinternals sin descargarlas.
- **Requisitos:** Cliente WebDAV y Descubrimiento de Red habilitado.
- **Versatilidad:** Ejecuta herramientas desde la línea de comandos o mapea una unidad de red.

## Preguntas y Respuestas

### ¿Cómo se ejecuta Process Monitor desde Sysinternals Live?

**Respuesta:** Utiliza la sintaxis `\\live.sysinternals.com\tools\procmon.exe`. Asegúrate de que el cliente WebDAV esté instalado y en funcionamiento y que el Descubrimiento de Red esté habilitado.

### ¿Qué es necesario para ejecutar herramientas Sysinternals desde la web en Windows Server 2019?

**Respuesta:** Necesitas instalar el componente WebDAV Redirector, que no viene instalado por defecto en Windows Server 2019. Usa PowerShell para la instalación y reinicia el servidor para completarla.

### ¿Cuáles son los dos métodos para ejecutar herramientas Sysinternals desde la web?

**Respuesta:**

1. **Desde la Línea de Comandos:** Ejecutando la herramienta directamente desde la línea de comandos.
2. **Desde una Unidad de Red Mapeada:** Creando y utilizando una unidad de red mapeada para ejecutar la herramienta.

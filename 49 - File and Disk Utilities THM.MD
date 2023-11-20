# Herramientas Sysinternals: Sigcheck, Streams y SDelete

## Explicación Detallada y Amplia

Las herramientas Sysinternals ofrecen una amplia gama de utilidades para la administración y seguridad de sistemas Windows. En esta sección, nos centraremos en tres herramientas específicas: Sigcheck, Streams y SDelete.

### Sigcheck

**Definición Oficial:** Sigcheck es una utilidad de línea de comandos que muestra el número de versión del archivo, información de tiempo y detalles de la firma digital, incluidas las cadenas de certificados. También ofrece una opción para verificar el estado de un archivo en VirusTotal y una opción para subir un archivo para escanearlo.

#### Caso de Uso: Verificar archivos sin firmar en C:\Windows\System32.

**Comando:** `sigcheck -u -e C:\Windows\System32`

- `-u`: Si la verificación de VirusTotal está habilitada, muestra archivos desconocidos por VirusTotal o con detecciones no nulas, de lo contrario, muestra solo archivos sin firmar.
- `-e`: Escanea imágenes ejecutables solamente (independientemente de su extensión).

![Captura de pantalla ejecutando sigcheck](/images/sigcheck001.png)
![Captura de pantalla ejecutando sigcheck](/images/sigcheck002.png)

### Streams

**Definición Oficial:** Streams es una herramienta que revela los flujos de datos alternativos (ADS) en NTFS. NTFS permite más de un flujo de datos en los archivos, pero el Explorador de Windows no muestra estos datos. Los escritores de malware han usado ADS para ocultar datos, pero no todos sus usos son maliciosos.

#### Ejemplo: Un archivo descargado de Internet.

**Uso:** Revelar identificadores escritos en ADS para archivos descargados de Internet.

![Captura de pantalla ejecutando streams](/images/streams1.png)
![Captura de pantalla ejecutando streams](/images/streams2.png)
![Propiedades del archivo de SysinternalsSuite.zip](/images/streams3.png)

### SDelete

**Definición Oficial:** SDelete es una utilidad de línea de comandos que permite eliminar archivos y/o directorios o limpiar el espacio libre en un disco lógico. Implementa el protocolo DOD 5220.22-M (protocolo de borrado y saneamiento del Departamento de Defensa de EE. UU.).

#### Uso por Adversarios:

- Asociado con las técnicas MITRE T1485 (Destrucción de Datos) y T1070.004 (Eliminación de Indicadores en el Host: Eliminación de Archivos).
- ID MITRE: S0195.

![Implementación del método de borrado DoD 5220.22-M](/images/DoDsdelete.png)
[Fuente](https://www.lifewire.com/dod-5220-22-m-2625856)

## Resumen

- **Sigcheck:** Utilidad para mostrar información y verificar firmas digitales de archivos.
- **Streams:** Revela flujos de datos alternativos en NTFS, útil para identificar archivos descargados de Internet.
- **SDelete:** Permite eliminar de forma segura archivos y directorios o limpiar espacio libre en un disco.

## Puntos Clave

- **Sigcheck:** Útil para verificar archivos sin firmar y su estado en VirusTotal.
- **Streams:** Importante para revelar información oculta en flujos de datos alternativos.
- **SDelete:** Herramienta esencial para borrado seguro de archivos, implementando protocolos del Departamento de Defensa.

## Preguntas y Respuestas

### ¿Qué hace Sigcheck y cómo se utiliza?

**Respuesta:** Sigcheck muestra información de archivos, como la versión y detalles de la firma digital. Se utiliza con el comando `sigcheck -u -e C:\Windows\System32` para verificar archivos sin firmar en un directorio específico.

### ¿Cómo funciona Streams y qué revela?

**Respuesta:** Streams revela flujos de datos alternativos en NTFS, como los identificadores de archivos descargados de Internet. Es útil para descubrir información que el Explorador de Windows no muestra.

### ¿Para qué se utiliza SDelete y qué protocolo implementa?

**Respuesta:** SDelete se utiliza para la eliminación segura de archivos y directorios, implementando el protocolo DOD 5220.22-M. Es relevante en contextos de seguridad y ha sido utilizado en técnicas de destrucción de datos y eliminación de indicadores en el host.

### Ejemplo: Hay un archivo txt en el escritorio llamado file.txt. Utilizando una de las tres herramientas analizadas en esta tarea, ¿cuál es el texto dentro del ADS?

**Respuesta:**

```powershel
cd Desktop
streams .\file.txt -accepteula
Get-Item .\file.txt -stream *
more .\file.txt:ads.txt
```

![Captura de pantalla ejecutando streams Ejemplo](/images/streamsExample.png)

[Tutorial de sala](https://www.youtube.com/watch?v=EhFuvNFf-ok&ab_channel=CyberInsight)

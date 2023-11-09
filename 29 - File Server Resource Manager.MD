# Administrador de Recursos del Servidor de Archivos (FSRM)

## Explicación Detallada

El **Administrador de Recursos del Servidor de Archivos (FSRM)** es una utilidad de Windows Server que se instala a través de 'Roles y Características' para gestionar los recursos compartidos en el servidor. FSRM permite acciones como:

- Limitar tipos de archivos que los usuarios pueden subir para prevenir malware.
- Crear cuotas para evitar que los usuarios llenen el servidor con datos excesivos.

### Ejemplos de Uso

- **Cuotas de Ficheros**: Impone límites de almacenamiento para los usuarios.
- **Filtrado de Archivos**: Bloquea tipos de archivos específicos, como ejecutables, para aumentar la seguridad.
- **Notificaciones**: Envia correos a los administradores cuando los usuarios alcanzan sus límites de cuota.

## Resumen

FSRM es una herramienta potente para gestionar cómo y qué datos se almacenan en los recursos compartidos del servidor. Proporciona control sobre las cuotas de almacenamiento y el tipo de archivos que se pueden subir, además de generar informes y notificaciones automáticas.

### Palabras Clave

- FSRM
- Cuotas
- Filtro de Archivos
- Notificaciones
- Seguridad de Datos

## Puntos Clave

- **Gestión de Cuotas**: Permite establecer límites suaves (avisos) o duros (bloqueo de subida) en el almacenamiento de datos.
- **Filtrado de Archivos**: Evita la subida de tipos de archivos peligrosos o no deseados.
- **Automatización**: Genera informes y realiza tareas de administración de archivos automáticamente según condiciones y horarios definidos.

## Preguntas y Respuestas

### ¿Qué es FSRM y para qué se utiliza?

FSRM es una herramienta de Windows Server para la gestión de recursos compartidos, que permite establecer políticas sobre los datos que los usuarios pueden almacenar en el servidor.

### ¿Cómo se puede instalar FSRM?

FSRM se instala a través de la sección 'Roles y Características' en la configuración de Windows Server, específicamente bajo 'Servicios de archivo e iSCSI'.

### ¿Qué beneficios ofrece FSRM para la administración de un servidor de archivos?

FSRM proporciona herramientas para controlar el tamaño y tipo de datos almacenados, evitar la saturación del servidor con datos excesivos, y mejorar la seguridad mediante el filtrado de archivos, junto con la capacidad de monitorear y reportar el uso de los recursos compartidos.

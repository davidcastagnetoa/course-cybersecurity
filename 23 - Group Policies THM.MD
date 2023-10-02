## Políticas de Grupo en Active Directory

Active Directory permite organizar usuarios y computadoras en unidades organizativas (OUs). La razón principal para hacerlo es poder aplicar diferentes políticas para cada OU.

### **Palabras clave**:

- OU (Unidad Organizativa)
- GPO (Política de Grupo)
- SYSVOL (directorio en Controladores de Dominio)

### GPOs (Políticas de Grupo)

Windows maneja estas políticas a través de **GPOs**. Una GPO es esencialmente un conjunto de configuraciones que se pueden asignar a OUs. Con GPOs, se pueden establecer configuraciones específicas para máquinas o identidades específicas.

Por ejemplo, en nuestro dominio, podemos ver que hay tres GPOs:

- Política de dominio por defecto
- Política RDP
- Política por defecto de controladores de dominio

### Edición de GPOs

La edición de una GPO se realiza a través de una herramienta especializada, y dentro de ella se pueden ver y modificar muchas configuraciones, como políticas de contraseña.

📌 **Ejemplo**: Cambiamos una política para que las contraseñas tengan un mínimo de 10 caracteres.

### Distribución de GPOs

Las GPOs se distribuyen a través de un recurso compartido de red llamado **SYSVOL**. Los usuarios sincronizan sus GPOs desde aquí. Cualquier cambio en las GPOs podría tardar hasta 2 horas en propagarse a todas las máquinas, ¡pero se puede forzar con el comando `gpupdate /force`!

### Creando GPOs para THM Inc.

1. **Restringir el acceso al Panel de Control**: Solo queremos que el departamento de IT tenga acceso. Creamos una GPO para ello y la vinculamos a las OUs de los usuarios que NO queremos que tengan acceso.

2. **Bloqueo automático de pantalla**: Queremos que las estaciones de trabajo y servidores se bloqueen automáticamente después de 5 minutos de inactividad. Se puede aplicar esta GPO al dominio raíz.

🔑 **Nota**: Si una GPO no funciona inmediatamente, ¡no olvides probar con `gpupdate /force`!

### Resumen:

Las OUs en Active Directory permiten agrupar usuarios y máquinas. Las GPOs nos permiten aplicar políticas específicas a estas OUs. Puedes pensar en las GPOs como "reglas" que decides para diferentes grupos de usuarios o computadoras. Por ejemplo, si no quieres que ciertos usuarios accedan al Panel de Control, ¡hay una GPO para eso!

<!-- https://youtu.be/dwP4jpXdSp4?si=uAjwC_GF-WnMs378&t=2872 -->

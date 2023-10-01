# Explicación detallada:

**Active Directory Domain Service (AD DS)** es el corazón de cualquier dominio de Windows. Funciona como un catálogo que almacena información sobre todos los "objetos" presentes en una red. Estos objetos pueden incluir usuarios, grupos, máquinas, impresoras, carpetas compartidas, entre otros.

1. **Usuarios:**

   - Son uno de los objetos más comunes en Active Directory. Hay dos tipos de "usuarios":
     - **Personas:** Representan a individuos en una organización que necesitan acceder a la red.
     - **Servicios:** Representan a servicios específicos como IIS o MSSQL.

2. **Máquinas:**

   - Cada computadora que se une al dominio de Active Directory se registra como un objeto "máquina". Estas máquinas son consideradas "principios de seguridad", lo que significa que tienen una cuenta con derechos limitados dentro del dominio.

3. **Grupos de seguridad:**

   - Ayudan a gestionar derechos de acceso a recursos. Los grupos pueden tener tanto usuarios como máquinas como miembros.

4. **Active Directory Users and Computers:**

   - Es una herramienta que se utiliza para configurar usuarios, grupos o máquinas en Active Directory.

5. **Unidades Organizativas (OUs):**

   - Son contenedores que permiten clasificar usuarios y máquinas. Son esenciales para definir conjuntos de políticas para diferentes departamentos o roles.

6. **Grupos de Seguridad vs OUs:**

   - Aunque ambos se utilizan para clasificar usuarios y computadoras, tienen propósitos distintos. Las OUs se usan para aplicar políticas y los grupos de seguridad para otorgar permisos.

     | Grupo de Seguridad                | Descripción                                                                                                                                                                                               |
     | --------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
     | **_Administradores del Dominio_** | _Los usuarios de este grupo tienen privilegios administrativos sobre todo el dominio. Por defecto, pueden administrar cualquier computadora en el dominio, incluidos los Controladores de Dominio (DCs)_. |
     | **_Operadores de Servidor_**      | _Los usuarios en este grupo pueden administrar los Controladores de Dominio. No pueden modificar las membresías de grupos administrativos._                                                               |
     | **_Operadores de Respaldo_**      | _Los usuarios en este grupo pueden acceder a cualquier archivo, ignorando sus permisos. Se utilizan para realizar copias de seguridad de datos en las computadoras._                                      |
     | **_Operadores de Cuenta_**        | _Los usuarios en este grupo pueden crear o modificar otras cuentas en el dominio._                                                                                                                        |
     | **_Usuarios del Dominio_**        | _Incluye todas las cuentas de usuario existentes en el dominio._                                                                                                                                          |
     | **_Computadoras del Dominio_**    | _Incluye todas las computadoras existentes en el dominio._                                                                                                                                                |
     | **_Controladores de Dominio_**    | _Incluye todos los Controladores de Dominio (DCs) existentes en el dominio._                                                                                                                              |

# Resumen (con ejemplos y palabras clave):

Imagínate **Active Directory (AD)** como un gran directorio telefónico para tu red. En este "directorio", tienes:

- **Usuarios:** Personas como Juan o servicios como un programa de correo.
- **Máquinas:** Computadoras como la laptop de Juan o el servidor de la oficina.
- **Grupos de Seguridad:** Imagina un club VIP donde solo ciertos usuarios tienen acceso a ciertos recursos.
- **Unidades Organizativas (OUs):** Son como secciones en el directorio, donde los miembros del equipo de ventas están en una página y el equipo de IT en otra.

En resumen, **AD** te ayuda a organizar y gestionar todos los recursos y usuarios en tu red. Es como un libro de reglas y directorio combinados.

## Puntos Clave:

- **Active Directory** organiza y controla toda una red.
- Los **usuarios** pueden ser personas o servicios.
- Las **máquinas** son las computadoras en la red.
- Los **grupos de seguridad** gestionan el acceso.
- Las **OUs** definen conjuntos de políticas para diferentes roles.

## Ejemplo

Para configurar usuarios, grupos o máquinas en Active Directory, debemos iniciar sesión en el Controlador de Dominio y ejecutar "Usuarios y Computadoras de Active Directory" desde el menú de inicio:

![Active Directory Users and Computers](/images/activedirectory.png)

Al abrir la ventana, puedes visualizar la jerarquía de usuarios, computadoras y grupos en el dominio. Estos se organizan en Unidades Organizativas (OUs), que son contenedores para clasificar usuarios y máquinas según necesidades específicas. Por ejemplo, el departamento de Ventas y el de IT tendrán diferentes políticas. Cada usuario pertenece a una única OU. Es común que las OUs reflejen la estructura de la empresa, como el OU "THM" que tiene sub-OUs para IT, Gestión, Marketing y Ventas. Aunque este es el modelo típico, puedes crear OUs según lo desees, como agregar una OU "Estudiantes" a "THM".

![Active Directory Users and Computers](/images/AD01.png)

Si abre alguna unidad organizativa, puede ver los usuarios que contiene y realizar tareas simples como crearlas, eliminarlas o modificarlas según sea necesario. También puede restablecer las contraseñas si es necesario (muy útil para el servicio de asistencia técnica):

![Active Directory Users and Computers](/images/AD02.png)

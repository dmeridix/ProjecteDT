# ProjecteDT


DAW:



DAM:

Esta aplicación está diseñada para tres tipos de usuarios: **Alumno**, **Profesor** y **Administrador**. Cada tipo de cuenta tiene diferentes permisos y funciones específicas. 

- **Objetivo para el alumno**: Consultar sus registros de asistencia, retrasos, y datos personales.
- **Objetivo para el profesor**: Consultar su información personal, gestionar sus grupos, pasar lista, y administrar su horario.
- **Objetivo para el administrador**: Supervisar los registros de asistencia y gestionar alertas de asistencia para los alumnos.

---

## 1. Funcionalidad del Alumno

Al iniciar sesión, el alumno verá un **calendario** con un resumen de su asistencia, donde se destacan en rojo los días de retrasos o ausencias. También verá su información personal registrada en la base de datos. En el menú superior, dispone de dos opciones principales:

![Imagen del calendario de alumno](https://github.com/user-attachments/assets/28a1886b-1515-4eab-b97d-50e86c9f3875)

### 1.1. Marcajes
En esta sección, el alumno puede consultar sus registros de asistencia. Cada registro muestra la **fecha**, **hora** y el **ID de marcaje**, correspondiente a su tarjeta o chip RFID (cada uno con un ID único).

![Imagen de marcajes](https://github.com/user-attachments/assets/c6b99d87-2b4b-47ba-ad7d-040d00d71612)

---

## 2. Funcionalidad del Profesor

Al iniciar sesión, el profesor verá una **tabla con sus grupos asignados**, donde puede consultar la asistencia de cada grupo, incluyendo el ID del grupo, nombre, y aula asignada. También verá su información personal. En el menú superior, dispone de opciones para **pasar lista** y **consultar horarios**.

![Imagen de grupos del profesor](https://github.com/user-attachments/assets/4b714e26-9509-4a8a-a61a-61eea5a81c6e)

### 2.1. Pasar Lista
En esta sección, el profesor puede pasar lista de asistencia para el grupo seleccionado desde el menú desplegable. La lista es **desplazable**, adaptándose al número de alumnos. En la parte inferior, dispone de dos botones: uno para **modificar la lista** y otro para **guardar** la asistencia.

![Imagen de pasar lista](https://github.com/user-attachments/assets/323ae17e-3b4c-4692-b300-f4088520df1d)

### 2.2. Horarios
En la sección de horarios, el profesor puede ver su horario en forma de tabla, que incluye **hora**, **nombre del curso** y **ID del curso**. Además de visualizar su horario, puede subir uno nuevo mediante un archivo Excel, el cual se almacenará en el servidor al presionar el botón de guardar.

![Imagen de horarios](https://github.com/user-attachments/assets/4ff6d7c3-4762-463e-b155-53cfd36c5df0)

---

## 3. Funcionalidad del Administrador

Al iniciar sesión, el administrador verá una **tabla con los marcajes recientes** que muestra el ID y fecha de cada registro de asistencia. En el menú superior, dispone de tres opciones principales:

![Imagen de la vista del administrador](https://github.com/user-attachments/assets/335c63d3-7557-4a94-a27b-5063feeac273)

### 3.1. Editar Marcaje
En esta sección, el administrador puede modificar el estado de los marcajes (presencia, ausencia, retraso). También puede **notificar al alumno** en caso de excesivas ausencias o retrasos. Los cambios solo se guardarán al presionar el botón de guardar.

![Imagen de editar marcaje](https://github.com/user-attachments/assets/84615e49-46ff-41ea-90e0-437be3f863f3)

### Otras Funcionalidades
Además de las funcionalidad de ediatr marcaje, el administrador tiene acceso a las mismas opciones que los usuarios **Alumno** y **Profesor** (pasar lista y horarios).


# Guía de Estilos

## Tipografía
La tipografía utilizada en toda la aplicación es **Inter**, una fuente moderna y legible que asegura una buena experiencia de usuario. Se utiliza **negrita** para resaltar las diferentes secciones de la página, así como para destacar el encabezado principal de la aplicación.

![image](https://github.com/user-attachments/assets/62f7c5b5-6d54-4761-97fd-014166796385)

## Estilo de Colores
Se ha utilizado una paleta de colores consistente en toda la aplicación y la página web. El **encabezado** (header) se distingue claramente del resto del contenido a través de un color de fondo diferente, lo que facilita la navegación.

![Imagen de la paleta de colores](https://github.com/user-attachments/assets/c5058590-ba81-46c5-ba65-bd5ede9ae81b)

## Tamaño de Letra
Se han establecido diferentes tamaños de fuente para diferenciar **títulos** y **contenido** de manera clara. Además, los botones tienen un tamaño de letra optimizado para asegurar su legibilidad y facilitar la interacción del usuario.

![Imagen del tamaño de la letra](https://github.com/user-attachments/assets/d3d9707a-4f38-401d-ad4c-fc4c680f9b3a)
![Imagen del tamaño de la letra de los botones](https://github.com/user-attachments/assets/a8102935-762d-4091-8d21-a2ba6d812920)

## Componentes (Botones y Controles)
Se han utilizado **componentes interactivos**, como botones, para conectar diferentes páginas de la aplicación. Para mejorar la usabilidad, cuando el usuario está en una página específica, el botón correspondiente en el menú cambia a un tono gris, indicándole su ubicación actual.

![Imagen de botones del menú](https://github.com/user-attachments/assets/71c887cb-f035-4942-a0a4-917228b7cb18)

Además, se ha implementado un **panel desplegable** para mostrar de manera ordenada los diferentes grupos, facilitando la navegación y la consulta de información.

![image](https://github.com/user-attachments/assets/8ad0ab98-1d94-47a3-b3d3-31e1c2718189)


Para las funciones que implican la **subida de archivos**, se ha utilizado un componente visual que simula un área para arrastrar y soltar archivos, asegurando una experiencia de usuario intuitiva.

![Imagen del componente de subida de archivos](https://github.com/user-attachments/assets/e2c6d690-e98c-4e99-9482-eadda270e903)

## Iconos
Se han integrado **iconos** gráficos en la interfaz, como las flechas, para indicar que ciertas áreas de la página tienen un comportamiento desplegable y mostrar más información al interactuar con ellas.

![image](https://github.com/user-attachments/assets/cc42535c-2cf4-48bd-b32a-ae3e6993b3f4)


## Enlace a Figma
Para visualizar y explorar los wireframes de la aplicación, puedes acceder al siguiente enlace de Figma:

[Figma Wireframe Projecte](https://www.figma.com/design/Pzd7ATRbGheYRKQswwkhY5/Wireframe-projecte?node-id=1-2&t=qHNvOIDonUpMxWAL-1)




---
## Enlace Figma
https://www.figma.com/design/Pzd7ATRbGheYRKQswwkhY5/Wireframe-projecte?node-id=1-2&t=qHNvOIDonUpMxWAL-1

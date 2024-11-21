# ProjecteDT

Diseño Base datos:

![image](https://github.com/user-attachments/assets/6c8b62ca-4a9f-4686-a406-8800bac42021)

Descripción de las tablas

Grupo:
Define els grups dins de l’organització, com ara classes d’estudiants o equips de treball.
Cada grup té un ID únic, un nom, una descripció, i un horari associat.

Permiso:
Representa permisos específics (per exemple, accés a determinades funcions o àrees).
Inclou un ID únic, un nom (exemple: "Gestionar alumnes") i una descripció del que permet fer.

Rol:
Defineix els rols que tenen els usuaris (per exemple, Alumne, Professor o Administrador).
Conté un ID únic, un nom, una descripció, i està relacionat amb la taula permiso per indicar quins permisos s’associen al rol.

Persona:
Emmagatzema les dades de les persones registrades (alumnes, professors o administradors).
Té un ID únic, informació personal com nom, cognom i DNI, i està relacionada amb un grup (grupo_id) i un rol (rol_id).
També inclou un camp aula per assignar una ubicació específica.

Tarjeta:
Registra les targetes RFID assignades a les persones per identificar-les.
Cada targeta té un ID únic, un codi RFID, una referència a una persona, la data d’assignació, i un estat (Activa o Inactiva).

RegistroTarjeta:
Registra les lectures de les targetes RFID.
Cada registre inclou un ID únic, una referència a una targeta (tarjeta_id), la data de lectura, i el tipus de lectura (Entrada o Salida).

Explicació del funcionament
Registre d’un alumne o professor
1.  Creació del grup:
- Es registra un grup a la taula grupo amb el nom i l’horari (per exemple, "Grup 1A", horari "8:00-14:00").
- Es genera un grupo_id automàticament.
 
2. Definició del rol:
- Es defineix un rol a la taula rol (exemple: "Professor").
- Es vincula el rol amb un permís específic a la taula permiso (exemple: "Pot modificar assistència").
- Es genera un rol_id.
  
3.Registre de la persona
- Es registra la persona a la taula persona amb les dades personals, el grupo_id, i el rol_id.
Exemple: "Joan Pérez", assignat al grup "Grup 1A" i amb rol de "Professor".
- L’ID de la persona (persona_id) es genera automàticament.
  
4.Assignació de la targeta RFID
- Es registra una targeta RFID a la taula Tarjeta amb un codi únic.
- Es vincula la targeta amb el persona_id de la persona assignada.
- Es defineix l’estat com Activa.

  
Ús del sistema i permisos
- Quan una persona fa servir la targeta, es registra a RegistroTarjeta:
- Es llegeix el codi de la targeta, es busca a Tarjeta per obtenir el id i la persona associada.
- S'insereix un registre a RegistroTarjeta amb el tipus de lectura (Entrada o Salida).
- 
Els rols determinen què pot fer la persona:
- Un alumne pot veure la seva pròpia informació (consultant la seva fila a persona).
- Un professor pot veure i modificar l’assistència dels alumnes del seu grup (consultant a grupo).
- Un administrador té accés complet a totes les dades i registres.

DAW:
Para el apartado de crear un wireframe d'aplicació web en FIGMA lo dividiremos en difentes secciones para que los usuarios que quieran hacer su registro de fichaje puedan llevar un control de fichaje de ellos mismos.
El objetivo és la creación de un sistema de fichaje para una institución donde quede registrado quien entra y sale una persona de una empresa como en el trabajo, lo que haremos es una pagina web donde cuando entren a la pagina puedan registrarse y luego iniciar sesión para asi saber quien esta entrando y que sus datos queden registrados en la base de datos del registro.

1. Para ello empezaremos en la primera pagina que es una bienvenida que da a los usuarios que entren de cual es la función principal de esta pagina que es la de hacer un control de fichaje en tiempo real, y un apartado de contacto por si llegan a tener algun problema a la hora de hacer el registro.

![image](https://github.com/user-attachments/assets/82459c3b-4af1-422a-87b4-9ff95b324db3)



2. En la primera pagina hemos visto que en el apartado del 'HEADER', hay diferentes botones al lado del logo y el nombre de la pagina, tenemos el botón para registrarse o iniciar sesión, para los usuarios que lleguen a la empresa por un ejemplo tendran la opción de 'iniciar sesión' y cuando le dan les aparecera la pagina para iniciar sesión y darle a la opción 'Continuar con Google' y seleccionar su correo de empresa o personal y ya con eso se les hara un registro automaticamente de ese usuario. Y cuando otro dia quieran iniciar sesión otra vez como se le ha cerrado la sesión directamente pone el correo suyo y ya podra acceder.

![image](https://github.com/user-attachments/assets/66c7a1f0-4067-4251-a766-2d8937a4d39d)



3. Si no tenemos una cuenta creada, podemos registrarla con tus datos personales para que queden guardados en la base de datos de la web con sus secciones para poner el nombre, apellidos y mas informaticón tuya, luego aceptar las condiciones de la pagina y un boton que
  dice 'CREA TU CUENTA' que al darle al boton ya tendras hecho el registro con tu correo y ya poder iniciar sesión para poder hacer tu fichaje y se quede guardado en la base de datos en este caso en el historial de registro.
![image](https://github.com/user-attachments/assets/a7f56ddc-49b3-4d1a-802d-73e6612bc906)




5. Una vez que ya hemos el registro y ya podemos acceder al apartado para hacer el registro y mirar el historial de registro, procederemos a ver la funcionalidad de esta pagina y como funciona, vemos que una vez dentro hay un apartado que pone 'Instruccions', que nos explicara como hacer el registro y tendremos dos botones, uno que es para ir a la pagina del registro y el otro es para ver el historial para comprobar que se ha hecho el registro correctamente.
![image](https://github.com/user-attachments/assets/48324844-408c-4b8e-a8fd-80227f9ef46a)



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

Wireframe APP:![image](https://github.com/user-attachments/assets/62f7c5b5-6d54-4761-97fd-014166796385)

Wireframe WEB:![image](https://github.com/user-attachments/assets/6f2821f0-043b-4b0f-b090-7f5614b8253b)


## Estilo de Colores
Se ha utilizado una paleta de colores consistente en toda la aplicación y la página web. El **encabezado** (header) se distingue claramente del resto del contenido a través de un color de fondo diferente, lo que facilita la navegación.

Wireframe APP:![Imagen de la paleta de colores](https://github.com/user-attachments/assets/c5058590-ba81-46c5-ba65-bd5ede9ae81b)

Wireframme WEB:![image](https://github.com/user-attachments/assets/c896ef88-213e-4aa4-8a9a-f9ca411b2fd3)

## Tamaño de Letra
Se han establecido diferentes tamaños de fuente para diferenciar **títulos** y **contenido** de manera clara. Además, los botones tienen un tamaño de letra optimizado para asegurar su legibilidad y facilitar la interacción del usuario.

Wireframe APP:![Imagen del tamaño de la letra](https://github.com/user-attachments/assets/d3d9707a-4f38-401d-ad4c-fc4c680f9b3a)

Wireframe APP:![Imagen del tamaño de la letra de los botones](https://github.com/user-attachments/assets/a8102935-762d-4091-8d21-a2ba6d812920)

Wireframe WEB: ![image](https://github.com/user-attachments/assets/f11a8ba6-d743-4034-9b72-67c078bfd895)

Wireframe WEB: ![image](https://github.com/user-attachments/assets/7f4f56ee-b183-4b3b-99d6-733c54ba4d38)


## Componentes (Botones y Controles)
Se han utilizado **componentes interactivos**, como botones, para conectar diferentes páginas de la aplicación. Para mejorar la usabilidad, cuando el usuario está en una página específica, el botón correspondiente en el menú cambia a un tono gris, indicándole su ubicación actual.

Wireframe APP:![Imagen de botones del menú](https://github.com/user-attachments/assets/71c887cb-f035-4942-a0a4-917228b7cb18)

Además, se ha implementado un **panel desplegable** para mostrar de manera ordenada los diferentes grupos, facilitando la navegación y la consulta de información.

Wireframe APP:![image](https://github.com/user-attachments/assets/8ad0ab98-1d94-47a3-b3d3-31e1c2718189)

Wireframe WEB: ![image](https://github.com/user-attachments/assets/003222f8-e0fb-4909-9e70-8af47a3692e6)

Aqui tenemos un boton para 'Continuar' cuando se introduce el correo o otra opción que es 'Continuar con Google' para poder registrarte con un correo de Google.


Para las funciones que implican la **subida de archivos**, se ha utilizado un componente visual que simula un área para arrastrar y soltar archivos, asegurando una experiencia de usuario intuitiva.

Wireframe APP:![Imagen del componente de subida de archivos](https://github.com/user-attachments/assets/e2c6d690-e98c-4e99-9482-eadda270e903)

Wireframe WEB: ![image](https://github.com/user-attachments/assets/d05b3636-a83e-4227-84b6-4bc459f677b8)
Dos botones para enviar a la pagina de Registrar y poder hacer el fichaje de entrada y salida, y el otro es para enviarte al historial y poder ver tus últimos fichajes.


## Iconos
Se han integrado **iconos** gráficos en la interfaz, como las flechas, para indicar que ciertas áreas de la página tienen un comportamiento desplegable y mostrar más información al interactuar con ellas.

Wireframe APP:![image](https://github.com/user-attachments/assets/cc42535c-2cf4-48bd-b32a-ae3e6993b3f4)


## Enlace a Figma
Para visualizar y explorar los wireframes de la aplicación, puedes acceder al siguiente enlace de Figma:

[Figma Wireframe Projecte](https://www.figma.com/design/Pzd7ATRbGheYRKQswwkhY5/Wireframe-projecte?node-id=1-2&t=qHNvOIDonUpMxWAL-1)


Captura get marcages
![image](https://github.com/user-attachments/assets/603eb8f9-7c56-4181-bec5-33f444048bbe)
- En esta captura comprobamos que busca los marcajes que se han hecho de entrada y salida por parte de los usuarios. Vemos que en el registro de la base de datos guarda información de la ID del marcaje, la 'tarjeta_id' que es la identificación de la tarjeta que esta usando el usuario, seguimos con la 'fecha_lectura' que es de tipo 'DATETIME' que en este campo saldra la fecha y hora de cuando hizo el marcaje el usuario, y finalmente el tipo_lectura que tambien sera 'DATETIME' que aquí mostrara si ha hecho 'ENTRADA o SALIDA' por parte de la persona que haga el marcaje.

Captura get de un id en concreto de marcage
![image](https://github.com/user-attachments/assets/ed04ee33-6ece-4fbe-9160-90b7138f71bf)
- Aquí continuamos con el registro de la BBDD con los marcajes, pero en este caso podremos buscar la mediante la ID que registro queremos buscar, por ejemplo si queremos buscar la ID del usuario de cuantas veces a fichado, pues mediante la ID podremos buscar sus registros de fichaje y así llevar un control.

Captura get personas
![image](https://github.com/user-attachments/assets/3630b00e-eff9-49db-8ada-edf82b594b91)
- Aqui procederemos a ser lo mismo pero esta vez con el registro en la BBDD en el apartado de 'Persones', aquí mostrara los usuarios registrados en la BBDD cada una con su información para identificar quien es quien, mediante la ID, nombre, apellidos, dni y aula.

Captura get de un id en concreto de persona
![image](https://github.com/user-attachments/assets/85e82711-ddac-4440-b81c-fe42e56bf364)
- Y por último si queremos buscar a una persona en concreta la podremos buscar con su ID, que para buscar a una persona especifica y sabemos su ID lo prodremos hacer de la siguiente manera 'IP/persones/{ID}', con esto facilitara la busqueda de la persona con la ID.

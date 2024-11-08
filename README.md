# ProjecteDT


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



7. Ahora veremos como funciona el registro, vemos que tendremos tres funciones en esta pagina, en primer apartado nos aparecera nuestro nombre de usuario o correo para ver que somos nosotros quienes estamos haciendo el fichaje, abajo en el segundo apartado aparecera la fecha y la hora que estamos haciendo el fichaje para saber que estamos fichando a esa hora y que no nos confundamos por si estamos fichando antes de la hora de salida o despues de la hora de entrada.
Y por el último tenemos un desplejable que si le damos nos aparecera varias opciones como 'Almorzar' para avisar que a esa hora estamos desayunando en la hora de descanso y despues tenemos las hora de 'entrada' que es cuando llegas al trabajo y saber la puntualidad de los trabajadores o usuarios de la emmpresa o institución y por otro lado tenemos el de 'salida' que es para indicar a la hora que hemos salido del trabajo y así llevar un control de la persona.
![image](https://github.com/user-attachments/assets/1eca636b-a166-445e-8f03-ee322a344219)



8. Y por último tenemos la pagina de 'historia de registro', que aqui veremos el control de fichajes que llevamos, y tambien para ver que se alla guardado correctamente el fichaje en la pagina anterior del registro y que así la empresa o en la institutción vean los fichajes que lleva esa persona y así lleva el control de todas las personas.
![image](https://github.com/user-attachments/assets/fa29ebf5-62c1-4407-8cb0-e3785786534f)




DAM:
La aplicacion esta dividida en tres usuarios, la cuenta del alumno, la del professor y la del administrador. Cada tipo de cuenta tiene unas limitaciones y unas funciones actividas. El objectivo de la aplicación por parte del alumno es consultar en cualquier momento sus marcages, sus atrasos, su información personal. El objectivo por parte del profesor es consltar su infrmacion personal, sus grupos, pasar lista de los alumnos, crear un horario para el y/o subir un horario mediante archivo excel.

1. Al iniciar sesion en la aplicacion con una cuenta de un alumno lo que primero vera el usuario es un calendario donde se veran reflejados los dias que ha tenido un atraso o una abscencia que estara marcado en rojo, a continaucion vera la inforamcion personal que esta registrda en la base de datos. En el menu de la parte superior de la aplicacion tiene dos botones.
![image](https://github.com/user-attachments/assets/28a1886b-1515-4eab-b97d-50e86c9f3875)

  1.1. Marcage
   En este apartado del alumno puede consultar sus margaces donde le muestra la fecha y hora del marcage y el ID del marcage que es la tarjeta RFID o el chip RFID (cada tarjata o chip tiene un id diferente)
![image](https://github.com/user-attachments/assets/c6b99d87-2b4b-47ba-ad7d-040d00d71612)

2. Al iniciar sesion en la aplicacion con una cuenta de un profesor lo primero que vera es una tabla de sus grupos donde puede ver su assitencia, en la tabla se muestra el id del grupo, el nombre y la aula que tiene asignada, finalmente s emuestrala información personal del profesor. En el menu de la parte superior contiene dos botones, uno para passar lista y otro para ver sus horarios.
![image](https://github.com/user-attachments/assets/4b714e26-9509-4a8a-a61a-61eea5a81c6e)

  2.1. Pasar lista
   En este apartado del professor puede passar lista sobre los alumnos de la clase que tiene selcionada en el desplegable de arriba, esta lista funciona como un scroll dependiendo de la cantodad de alumnos que haya en al clase. Finalmente tiene dos botones en la parte inferior donde uno es para modificar la lista ya pasada y el otro para guardarla
![image](https://github.com/user-attachments/assets/323ae17e-3b4c-4692-b300-f4088520df1d)
   
  2.2. Horarios
   En este apartado del profesor puede ver su horario que esta implementado como una tabla que contiene la hora, el nombre del curso y el ID del curso. A parte de visualiar su horario tambien puede subir su horario mediante un archivo de excel que se guardara en el servidor, si no le da al boton de guardar no se guadara el horario.
![image](https://github.com/user-attachments/assets/4ff6d7c3-4762-463e-b155-53cfd36c5df0)
   
3. Al iniciar sesion en la aplicaicon con una cuenta de un administrador loprimero que se vera es un tabla con todos los marcages más recientes implementado con una tabla que muestra el id y la fecha del marcage. En el menu de la parte superior de la aplicacion tiene tres botones.
![image](https://github.com/user-attachments/assets/335c63d3-7557-4a94-a27b-5063feeac273)

   3.1 Editar marcage o modificar
   En este apartado del administrador puede editar el estado de los marcages si tienen algun algun atraso, abscencia o presencia. A parte de estaas funciones puede notificar al alumno en el caso de exceso de abscencias o atrasos, si no se acciona el boton de guardar no se guardaran las modificaciones o notificaciones.
![image](https://github.com/user-attachments/assets/84615e49-46ff-41ea-90e0-437be3f863f3)

   Las demas funcionalidades de los botones son las mismas explicadas anteriormente 





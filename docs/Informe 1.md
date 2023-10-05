# 1.SCM

## Repositorio Git

Se creó el repositorio remoto primero, asegurándome que este 

Posterior a esto creó el repositorio local utilizando "git clone" y el http del repositorio remoto
```
git clone https://github.com/LorenzoVig/Proyecto-FIS-2023S2-LorenzoViglieti279445.git
```
una Vez creado el repositorio empiezo a trabajar utilizando los siguientes comandos de git:

#### git status

Este comando me permite visualizar de manera rápida que cambios están y cuales faltan agregar a la staging area. además, señaliza en que branch uno está trabajando. De uso vital antes de un commit.

#### git add

Comando que agrega archivos y cambios al staging area.

#### git commit

El commit facilita el pase de objetos de la staging area al repositorio local, utilizamos el switch -m seguido por texto en comillas dobles para agregar el mensaje que explica que cambios han sido agregados a él repositorio local con el commit realizado.

#### git branch

El comando "git branch" seguido por un nombre crea un branch nuevo en el repositorio local, permitiendo trabajar en paralelo a el main y a otros branches, así logrando minimizar errores irreversibles en el código principal del proyecto.

#### git checkout

Este comando permite pasar de un branch del repositorio a otro.

#### git merge

Este Comando combina dos ramas del repositorio, lo utilizamos el terminar y asegurar el buen funcionamiento del trabajo hecho en una rama.

#### git push

Comando que empuja todos los cambios del repositorio local al repositorio remoto.

#### git pull

Comando que copia todos los cambios del repositorio remoto al repositorio local.

### Otros comandos no utilizados en esta entrega, pero de uso frecuente y de mucha utilidad: 

#### git stash y git stash pop

De increíble utilidad cuando se está trabajando al mismo tiempo en distintas partes de un mismo archivo. Stash guarda los cambios realizados en un "stash" y retorna los archivos al estado en el que estaban en su último push, permitiendo un fácil y limpio pull del repositorio remoto. El comando git stash pop reaplica los cambios guardados en el stash para poder seguir codificando.

## Versionado

Para poder trabajar de manera eficiente y correcta en el proyecto debemos asegurarnos de usar prácticas de buen versionado, primero y de manera más importante debemos trabajar en branches separadas del main, con el objetivo de solo tener en este las funciones implementadas en su estado final, funcionando sin ningunos errores. Así mismo es imperativo establecer buenos principios sobre como utilizaremos los repositorios del proyecto.

### Realizar un push del Código finalizado al fin de cada día y siempre realizar un pull antes de comenzar a codificar.

Esto asegurara que el Código siempre este actualizado y en funcionamiento. El realizar un pull, incluso cuando se cree estar en la versión más actual del proyecto, sirve para negar por completo la posibilidad de perder progreso y el realizar un push diario asegura que no haya redundancias en las tareas del equipo.

### Escribir mensajes de commit claros, explicando donde y que se ha modificado.

Es vital asegurarse de especificar en cada commit sobre que archivo se ha trabajado y que se ha hecho, se puede generalizar, pero es de gran utilidad especificar si se ha arreglado, agregado o borrado código, esto da una ayuda increíble en el caso de tener que volver a un commit anterior, además de proveer una historia fácil de entender del progreso en el proyecto.

### Nunca hacer commits de código sin finalizar

Todo código que es pasado a un repositorio debe ser funcional y completo. Es un requerimiento absoluto que el código que commiteamos esté finalizado y no tener ninguna instancia de código incompleto.

### Siempre testear antes de hacer un commit

Como dicho anteriormente todo código en los repositorios debe ser funcional. Debemos testear todo código antes de hacer un commit, para minimizar la chance de propagar más errores y no crear confusión sobre el funcionamiento del resto del proyecto.

### Trabajar en ramas separadas y solo mergear cuando una función sea funcional y no tenga errores.

Como dicho anteriormente la rama main debe contener exclusivamente el código finalizado que ha de ser presentado en el proyecto final. Es necesario que cualquier rama que agregue funcionalidades al proyecto sea testeada minuciosamente y que cumpla con todos los requerimientos de esta función para que se la fusione con la rama main. Si no se cumplen estos requerimientos se tendrá que continuar iterando sobre el código hasta cumplirlos.


# 2.Requerimientos

## Elicitación

### Analisis de GUI
#### Autogestion circulo catolico
Base los perfiles de las mascotas registradas en la autogestion de mi mutualista, el circulo catolico, es un sistema muy simple que permite con facilidad agendar fechas de consultas, ver que fechas hay agendadas y ver estudios anteriores.

Esto se hace mediante paginas separadas lo cual me parece un poco redundadnte, la pagina para agendar fechas cuenta con forms para especificar que medico se desea consultar seguido por un calendario y un formulario para especificar que dia y hora se desea agendar. En otra pagina se muestran las reservas presentes de el usuario en una lista simple ordenados por fecha mas cercana. Finalmente los estudios anteriores se encuentran en otra pagina que lista como pdf todos los estudios hechos hasta la fecha.

#### Petfinder
Petfinder.com es un sitio americano que permite buscar una lista de animales en adopcion en la zona de el usuario.

El sitio pide que especie de animal se quiere adoptar y la locacion o codigo zip del usuario para listar todas las mascotas de esa especie en adopcion en la zon del usuario. Se presenta una lista de cards con los nombres, edades, razas y la distancia del la zona donde esta la mascota, hay multiples filtros en el sitio que permiten especificar desde edad y tamañp hasta si son rescatados o no. 

### Entrevista a usuario prospectivo
Entrevista con Victoria Martínez, estudiante universitaria de comunicación.

- cuantas y que mascotas tiene?

"Tengo 4 gatos 2 de ellos rescatados"

-las lleva al veterinario a menudo?

"Los llevo al veterinario cuando se presenta un problema de salud o noto algo fuera de lo normal."

-como maneja las consultas al veterinario? Tiende a agendarse antes de ir?

"No, los tiendo a llevar cuando algun problema aparece. No agendamos una cita, simplemente vamos."

-cuando se les receta medicaciones a sus mascotas como controla el consumo de ellas?

"Para controlar la medicación seguimos las instrucciones del veterinario, tiendo a anotarlas en las notas del celular."

-si se le ofreciese una solucion para el control de salud de su mascota online, similar al de una mutualista, lo usaria?

"No la usaríamos, porque como dijimos vamos a la veterinaria cuando pasa algo, entonces no reservamos. Pero en si veo que tenga mucha utilidad para personas que lleven a sus mascotas a el veterinario mas a menudo."

##### Conclusion
Esta entrevista solidifico la necesidad de asgurarnos que nuestro sistema sea muy simple y de uso muy facil y con funcionalidades de utilidad general para poder lograr que dueños de mascotas menos constantes con el cuidado de sus animales puedan sacarle uso.

### User Personas

### Modelo Conceptual del Problema

## Especificación

### Requerimientos Funcionales y No Funcionales

###### RF1 - Mascotas
El sistema deberá permitir acceder a una lista de todas las mascotas registradas del usuario, detallando:
* Nombre de la mascota
* Historia clinica de la mascota
* Proxima fecha de chequeo/Vacunacion
* Medicaciones asignadas a la mascota y la cantidad de dosis

###### RF2 - Agendar Horas con Veterinario
Se debera mediante formularios en los perfiles de cada mascota agendar una hora con el veterinario para un chequeo con la mascota especificada.
* Debera haber un calendario que permita seleccionar las fechas
* Un combo que permita seleccionar las hora de el chequeo.

###### RF3 - Modificacion de registro
El sistema debe permitir la modificación de la historia clinica y los medicamentos recetados de las mascotas registradas por el veterinario.

###### RF4 - Proxima fecha actualizada
Despues de reservar una hora con el veterinario la proxima fecha de chequeo/vacunacion debe actualizarse de inmediato.

###### RF5 - Registro de Mascotas
Se debera poder registrar mascotas al sistema mediante un tab en la pagina de gestion de mascotas.
* Debe haber forms para el nombre, sexo, especie y raza requeridos para registrar a la mascota.
* Debe haber dos campos opcionales para registrar la historia clinica de la mascota y otro para registrar alergias y otras aflicciones de la mascota.

###### RF6 - Mascotas en adopcion
Debera haber un listado de las mascotas para adoptar en el sitio, detallando:
* Nombre de la mascota
* Sexo de la mascota
* Especie de la mascota
* Raza de la mascota

###### RF7 - Solicitud de adopcion
Los perfiles de mascotas en adopcion deben de contar con un boton en cada uno que abra una pestaña nueva a un chat de whatsapp para gestionar la adopcion de la mascota.

###### RF8 - Filtrado Animales
El sistema debera permitir el filtrar las mascotas en adopcion por especie, raza, sexo y edad de estas.

###### RNF1 - Responsiveness
El sistema deberá adaptarse y mostrarse sin errores en las pantallas de todos los telefonos mobiles modernos tanto como en pantallas de computadora.

###### RNF2 - Navegadores y Sistemas Operativos
El sistema deberá funcionar al menos en los siguientes navegadores y versiones:

* Google Chrome >= 102
* Firefox: >= 103
* Safari >= 14
* Opera >= 73
* Microsoft Edge >= 95

Y deberá funcionar al menos en los siguientes sistemas operativos y versiones:

* iOS >= 15
* Android >= 8
* Microsoft Windows >= 10
* macOS >= 11

###### RNF3 - Online
Para acceder a la aplicación, visualizar y solicitar la adopcion de un animal, getionar las horas con el veterinario y ver los perfiles de animales registrados, el sistema operativo o navegador del usuario debe de contar con conexión a Internet.

###### RNF4 - Tiempos de respuesta
Despues de registrar una mascota o reservar una hora con el veterinario, el ususario debe ver el cambio en el sitio en menos de 10 segundos.

###### RNF5 - Numero de clicks
El usuario debera poder acceder a todas las funcionalidades de el sistema en menos de 5 clicks cada una.

### User Stories
#### ID: #1

Título: Registro de Mascota

Narrativa: Como dueño de mascotas atareado quiero tener un registro al día de mi mascotas, para poder visulalizar y corroborar con facilidad que fechas debe asistir al veterinario, que medicaciones se le han recetado y su historia clinica por si se presenta la ocacion de necesitarla.
Criterios de Aceptación:

○ Cada usuario debe de tener registros actualizados de sus mascotas en los perfiles de cada una.

#### ID: #2

Titulo: Filtrado Animales

Narrativa: Como dueño de mascotas prospectivo quiero filtrar los animales en adopcion por especie, raza y edad para poder ver cuales se adaptarian mejor a mi hogar.

Criterios de Aceptación:

○ Puede filtrarse la lista de animales en adopcion por especie, raza y edad.

#### ID: #3

Titulo: Ingresar mascotas al sistema

Narrativa: Como dueño de multiples mascotas quiero poder ver a simple vista los perfiles de todas mis mascotas para corroborar que medicaciones fueron recetadas a ellas.

Criterios de Aceptación:

○ Los usuarios deben poder registrar multiples mascotas al sistema sin errores y poder visualizarlos de manera facil.

#### ID: #4

Titulo: Acceso de Historias clinicas

Narrativa: Como veterinario quiero ver las hisorias clinicas de las mascotas que se atienden conmigo para poder saber de tratamientos anteriores y que medicaciones se les fueron dados para saber como mejor atenderlos.

Criterios de Aceptacion:

○ Las historias clinicas de los animales deben ser de facil acceso y modificacion, ademas de estar en fecha.

#### ID: #5

Titulo: Contacto para adopcion

Narrativa: Como dueño de mascotas prospectivo quiero poder coordinar por whatsapp una fecha para conocer y decidir finalmente si voy a adoptar al animal elegido.
Criterios de Aceptacion:

○ La lista de animales en adopcion debe estar vinculada al whatsapp de el centro de adopcion para facilitar el uso de los usuarios.

## Use Cases

| Nombre          |    Visualizar lista de mascotas      |
|-----------------|--------------------------------------|
| Actor           |                       |
|-----------------|--------------------------------------|
| Accion de Actor |   Accion de Sistema   |
| Preciso        | Si  | Si  | Si  | Si   | 
| Verificable    | Si  | Si  | Si  | Si   |
| Prioritizado   | Si  | Si  | Si  | Si   |
# 3.Informe académico 1

## Técnicas aplicadas y aprendizajes
Se utilizo bastante los comandos para git, asegurando un ambiente de desarollo organizado, lo cual facilito la realizacion de las tareas. Especificamente se aprecia como se puede lograr hacer progreso en la tarea sin importar en la computadora que se realize.
Las tecnicas de elicitacion sirvieron de buena base para entender mejor como plantear el diseño del sistema y las de especificacion dan una muy buena lista de que va a ser necesario desarollar y mejorar para la sagunda entrega.
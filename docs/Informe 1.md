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

### Análisis de GUI
#### autogestión círculo católico
Base los perfiles de las mascotas registradas en la autogestión de mi mutualista, el círculo católico, es un sistema muy simple que permite con facilidad agendar fechas de consultas, ver que fechas hay agendadas y ver estudios anteriores.

Esto se hace mediante paginas separadas lo cual me parece un poco redundante, la página para agendar fechas cuenta con formas para especificar que medico se desea consultar seguido por un calendario y un formulario para especificar qué día y hora se desea agendar. En otra página se muestran las reservas presentes del usuario en una lista simple ordenados por fecha más cercana. Finalmente, los estudios anteriores se encuentran en otra página que lista como pdf todos los estudios hechos hasta la fecha.

#### Petfinder
Petfinder.com es un sitio americano que permite buscar una lista de animales en adopción en la zona del usuario.

El sitio pide que especie de animal se quiere adoptar y la locación o Código zip del usuario para listar todas las mascotas de esa especie en adopción en la zona del usuario. Se presenta una lista de cards con los nombres, edades, razas y la distancia de la zona donde está la mascota, hay múltiples filtros en el sitio que permiten especificar desde edad y tamaño hasta si son rescatados o no. 

### Entrevista a usuario prospectivo
Entrevista con Victoria Martínez, estudiante universitaria de comunicación.

- cuantas y que mascotas tiene?

"Tengo 4 gatos 2 de ellos rescatados"

-las lleva al veterinario a menudo?

"Los llevo al veterinario cuando se presenta un problema de salud o noto algo fuera de lo normal."

-como maneja las consultas al veterinario? ¿Tiende a agendarse antes de ir?

"No, los tiendo a llevar cuando algún problema aparece. No agendamos una cita, simplemente vamos."

-cuando se les receta medicaciones a sus mascotas como controla el consumo de ellas?

"Para controlar la medicación seguimos las instrucciones del veterinario, tiendo a anotarlas en las notas del celular."

-si se le ofreciese una solución para el control de salud de su mascota online, similar al de una mutualista, lo usaría?

"No la usaríamos, porque como dijimos vamos a la veterinaria cuando pasa algo, entonces no reservamos. Pero en si veo que tenga mucha utilidad para personas que lleven a sus mascotas a el veterinario más a menudo."

##### conclusión
Esta entrevista solidifico la necesidad de asegurarnos que nuestro sistema sea muy simple y de uso muy fácil y con funcionalidades de utilidad general para poder lograr que dueños de mascotas menos constantes con el cuidado de sus animales puedan sacarle uso.

### User Personas

### Modelo Conceptual del Problema

## Especificación

### Requerimientos Funcionales y No Funcionales

###### RF1 - Mascotas
El sistema deberá permitir acceder a una lista de todas las mascotas registradas del usuario, detallando:
* Nombre de la mascota
* Historia clínica de la mascota
* próxima fecha de chequeo/vacunación
* Medicaciones asignadas a la mascota y la cantidad de dosis

###### RF2 - Agendar Horas con Veterinario
Se deberá mediante formularios en los perfiles de cada mascota agendar una hora con el veterinario para un chequeo con la mascota especificada.
* Debería haber un calendario que permita seleccionar las fechas
* Un combo que permita seleccionar la hora de el chequeo.

###### RF3 - modificación de registro
El sistema debe permitir la modificación de la historia clínica y los medicamentos recetados de las mascotas registradas por el veterinario.

###### RF4 - próxima fecha actualizada
después de reservar una hora con el veterinario la próxima fecha de chequeo/vacunación debe actualizarse de inmediato.

###### RF5 - Registro de Mascotas
Se debería poder registrar mascotas al sistema mediante un tal en la página de gestión de mascotas.
* Debe haber formas para el nombre, sexo, especie y raza requeridos para registrar a la mascota.
* Debe haber dos campos opcionales para registrar la historia clínica de la mascota y otro para registrar alergias y otras aflicciones de la mascota.

###### RF6 - Mascotas en adopción
Debería haber un listado de las mascotas para adoptar en el sitio, detallando:
* Nombre de la mascota
* Sexo de la mascota
* Especie de la mascota
* Raza de la mascota

###### RF7 - Solicitud de adopción
Los perfiles de mascotas en adopción deben de contar con un botón en cada uno que abra una pestaña nueva a un chat de WhatsApp para gestionar la adopción de la mascota.

###### RF8 - Filtrado Animales
El sistema debe permitir el filtrar las mascotas en adopción por especie, raza, sexo y edad de estas.

###### RNF1 - Responsiveness
El sistema deberá adaptarse y mostrarse sin errores en las pantallas de todos los teléfonos móviles modernos tanto como en pantallas de computadora.

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
Para acceder a la aplicación, visualizar y solicitar la adopción de un animal, gestionar las horas con el veterinario y ver los perfiles de animales registrados, el sistema operativo o navegador del usuario debe de contar con conexión a Internet.

###### RNF4 - Tiempos de respuesta
después de registrar una mascota o reservar una hora con el veterinario, el usuario debe ver el cambio en el sitio en menos de 10 segundos.

###### RNF5 - Numero de clicks
El usuario debe poder acceder a todas las funcionalidades del sistema en menos de 5 clicks cada una.

### User Stories
#### ID: #1

Título: Registro de Mascota

Narrativa: Como dueño de mascotas atareado quiero tener un registro al día de mi mascota, para poder visualizar y corroborar con facilidad que fechas debe asistir al veterinario, que medicaciones se le han recetado y su historia clínica por si se presenta la ocasión de necesitarla.
Criterios de Aceptación:

○ Cada usuario debe de tener registros actualizados de sus mascotas en los perfiles de cada una.

#### ID: #2

Título: Filtrado Animales

Narrativa: Como dueño de mascotas prospectivo quiero filtrar los animales en adopción por especie, raza y edad para poder ver cuales se adaptarían mejor a mi hogar.

Criterios de Aceptación:

○ Puede filtrarse la lista de animales en adopción por especie, raza y edad.

#### ID: #3

Título: Ingresar mascotas al sistema

Narrativa: Como dueño de múltiples mascotas quiero poder ver a simple vista los perfiles de todas mis mascotas para corroborar que medicaciones fueron recetadas a ellas.

Criterios de Aceptación:

○ Los usuarios deben poder registrar múltiples mascotas al sistema sin errores y poder visualizarlos de manera fácil.

#### ID: #4

Título: Acceso de Historias clínicas

Narrativa: Como veterinario quiero ver las historias clínicas de las mascotas que se atienden conmigo para poder saber de tratamientos anteriores y que medicaciones se les fueron dados para saber cómo mejor atenderlos.

Criterios de Aceptación:

○ Las historias clínicas de los animales deben ser de fácil acceso y modificación, además de estar en fecha.

#### ID: #5

Título: Contacto para adopción

Narrativa: Como dueño de mascotas prospectivo quiero poder coordinar por WhatsApp una fecha para conocer y decidir finalmente si voy a adoptar al animal elegido.
Criterios de aceptación:

○ La lista de animales en adopción debe estar vinculada al WhatsApp del centro de adopción para facilitar el uso de los usuarios.

## Use Cases

| Nombre | agendar hora con veterinario |
| Actor | Usuario |
| Acción de Actor |   Acción de Sistema   |
|-----------------------------------------|
| 1. Selecciona "Gestión de Mascotas" en página inicial | 2. El sistema llama a la lista de mascotas del usuario y genera cards con la información de cada uno |
| 3. Selecciona en el card de la mascota deseada una fecha en el calendario, una hora en form y da click en el botón de agendarse | 4. El sistema recibe la f|
|Cursos alternativos: 1.1: El usuario no tiene mascotas registradas: al abrir "gestión de mascotas" salta un error diciendo "No hay mascotas registradas en el sistema" y |
# 3. Informe académico 1

## Técnicas aplicadas y aprendizajes
Se utilizo bastante los comandos para git, asegurando un ambiente de desarrollo organizado, lo cual facilito la realización de las tareas. Específicamente se aprecia como se puede lograr hacer progreso en la tarea sin importar en la computadora que se realice.
Las técnicas de elicitacion sirvieron de buena base para entender mejor como plantear el diseño del sistema y las de especificación dan una muy buena lista de qué va a ser necesario desarrollar y mejorar para la segunda entrega.
echa del calendario y la hora de el form y las envía al sistema para que quede agendado de inmediato se actualiza el estado de "próxima fecha agendada"
se abre el tab para registrar una mascota. 3.1: Si el usuario selecciona una fecha o hora invalida, no se habilita el boto de agendarse
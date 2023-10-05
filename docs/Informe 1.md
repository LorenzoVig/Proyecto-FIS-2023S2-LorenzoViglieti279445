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

## Especificación

# 3.Informe académico 1

## Técnicas aplicadas y aprendizajes
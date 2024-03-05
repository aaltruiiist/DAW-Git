#Manual de GIT

##Sistema de control de versiones 
Git es un sistema  de control de versiones. Este sistema permite realizar un seguimiento,una gestión y una revisión de todos los cambios de código de un software a lo largo del tiempo. 

Este sistema es fundamental para tener flujos de trabajo eficientes, permitiendo la contribución a una base de código compartida de forma independiente.

El sistema de control de versiones también actúa como un mecanismo de seguridad, permitiendo deshacer actualizaciones de código si ocurriese un error.

##Conceptos básicos
Antes de explicar el funcionamiento es preciso comentar algunos conceptos básicos:

Directorio
: Carpeta que contiene una copia de una versión concreta del proyecto con la que se está trabajando.

Staging area 
: Zona donde se guardan los cambios temporalmente desde el directorio de trabajo antes de hacerlos definitivos y registrarlos en el repositorio.

Repositorio
: Todo proyecto que está siendo seguido por GIT, el cual contiene un historial en el que se están registrando los cambios confirmados desde la zona temporal (staging area).

Ramas
: El proyecto puede contener varias bifurcaciones del estado del código, que sirven como nuevos camino para evolucionar el código, en paralelo con otras ramas. 

Clon
: Copia exacta del repositorio. Es lo primero que debe hacer un programador cuando se integra al equipo. Cada miembro de un grupo de trabajo tiene un clon del repositorio en su equipo local.

##Funcionamiento de Git
###Funcionamiento interno 
Git maneja los datos como una secuencia de copias instantáneas.

Tiene tres estados principales en los que se pueden encontrar los archivos:
**Confirmado:** Los datos están almacenados en la base de datos local.
**Modificado:** El archivo ha sido modificado, pero los cambios no se han confirmado a la base de datos.
**Preparado:** Se ha marcado un archivo previamente modificado para ser confirmado.

Por lo tanto, Git tiene tres secciones principales dentro de un proyecto:
**El directorio de Git:** Es lo que se copia cuando clonas un repositorio desde otro ordenador. Dentro se almacenan los metadatos y la base de datos de objetos.
**El directorio de trabajo:** Es una copia de una versión del proyecto. Se sacan de la base de datos y se colocan en el disco del ordenador para ser usados y modificados.
**El área de preparación:** Archivo que almacena información acerca de los cambios que vamos a confirmar en nuestra próxima confirmación.

###Funcionamiento externo 
Lo que hemos explicado hasta aquí se denomina flujo de trabajo, que se resume en los siguientes pasos:
1. Modificamos una serie de archivos en el directorio de trabajo.
2. Preparamos los archivos que queramos confirmar en el área de preparación.
3. Confirmamos los cambios, tomando los archivos del área de preparación y almacenando una copia instantánea de manera en el directorio de Git. 
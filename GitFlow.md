# GitFlow 

## ¿Qué es GitFlow?

GitFlow es un modelo alternativo que funciona mediante a la creación de ramas en Git, en el que existen ramas de función y varias ramas principales. 


## Ventajas y Motivos

1. **Separación de funcionalidades:** Promueve la separación de las funcionalidades en diferentes ramas:
     
    *Main o Ramas Principales*
    - Es la rama de desarrollo contiene el codigo estable y listo para produccion. 
     <br>
    *Features o Ramas de funcionalidades* 
    - Son las ramas que se crean para desarrollar nuevas funcionalidades o características, cada vez que se añade una nueva característica se crea una a partir del codigo de la rama principal. Cuando esta feature esta terminada y probada se fusiona de nuevo con la rama main.
    <br>
    *Releases o Ramas de Lanzamiento*
    - Se utilizan para preparar una versión para su lanzamiento, se crean a partir de la rama principal, cuando el proyecto se acerca a una nueva versión. En esta rama se pueden realizar pequeñas correciones previas a su despliegue.
    <br>
    *Hotfix o Ramas de Correción de Errores*
    - Estás ramas se utilizan para corregir errores criticon en producción. Se crean a partir de la rama principal y se pueden fusionar tanto con la rama de lanzamiento actual, si existe o con la misma rama principal.
    <br>
2. **Mayor control de versiones:** Gestionar las versiones es más facil gracias a las ramas específicas, ya que permite un mayor control sobre los cambios que se incluyen en cada versión y cuando desplegarla.
   <br>
3. **Facilita la colaboración:** Al especificar el manejo de las diferentes ramas y como se deben fusionar los cambios, permite que varias personas trabajen sobre el mismo codigo, pero reduciendo la posibilidad de conflictos en el codigo. 
   <br>
4. **Flexibilidad y Escalabilidad:** Puede adaptarse a diferentes tipos de proyectos y tamaños de equipo. Puede escalar fácilmente desde proyectos pequeños hasta proyectos más grandes y complejos, manteniendo una estructura coherente y organizada.
    <br>
5. **Revertir cambios:** Si algo sale mal con una característica o una versión, Git Flow permite revertir esos cambios de manera segura sin afectar otras partes del proyecto.
    <br>
6. **Compatibilidad con herramientas y servicios**: H ay muchas herramientas y servicios que están integrados o son compatibles con GitFlow, como plataformas de alojamiento de repositorios como GitHub, GitLab o Bitbucket, así como herramientas de integración continua y despliegue continuo (CI/CD).


## Desventajas

1. **Complejidad Incial:** Puede llegar a resultar complejo para usuarios que no esten relacionados con
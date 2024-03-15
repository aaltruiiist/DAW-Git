
# GitFlow 

- [GitFlow](#gitflow)
  - [¿Qué es GitFlow?](#qué-es-gitflow)
  - [Ventajas y Motivos](#ventajas-y-motivos)
  - [Desventajas](#desventajas)
  - [Alternativas a Git Flow](#alternativas-a-git-flow)
  - [Ejemplos de uso de Git Flow](#ejemplos-de-uso-de-git-flow)
- [Bibliografía](#bibliografía)
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

1. **Complejidad Incial:** Puede llegar a resultar complejo para usuarios que no esten familiarizados o no tienen experiencia previa en la gestión de ramas.
    <br>
2. **Mayos cantidad de ramas:** Implica la creación de múltiples rmas en comparación con otros flujos de trabajo.
    <br>
3. **Riesgos de conflicto:** Al existir más ramas, existe un mayor riesgo de conflicto durante la fusion de las mismas, especialmente en proyectos grandes o cuando varios desarrolladores trabajan en funcionalidades simultáneas.
    <br>
4. **Sobrecarga de mantenimiento:** Mantener las múltiples ramas puede llevar una sobrecarga de mantenimiento, mayoritariamente en proyectos pequeños o con recursos limitados.

## Alternativas a Git Flow

1. **GitLab Flow:**  Es una alternativa que nace a partir de las carencias que se detectaron en GitHub Flow y Git Flow. 
   El flujo consta de una rama master, ramas features y ramas de entorno; cada vez que se acaba una feature se hace un merge request a master. Cuando la rama master cuenta con varias features, se hace un merge request a preproducción y luego a producción.
   No se necesitan ramas release ya que cada entorno es desplegado con cada merge request aceptada.
    <br>
2. **Trunk-based Flow:** Este flujo presenta un cambio de filosofía:
   Los desarrolladores deben colaborar siempre sobre master.
   En casp de que una evolución compleja, se hace uso de features flags para activar o desactivar nuevas características.
   Se prefiere la metodología Pair-Programming (Dos personas trabajando en paralelo sobre el mismo código).
    <br>
3. **Master-only Flow:** Este flujo de trabajo usa solo una rama, la cual es infinita. Se realizan features y hot-fix sobre la misma rama y se testean en local con un commit, cuando se aprueba el nuevo cambio se hace un push contra la rama principal y se despliega en producción al instante.
   <br>
4. **GitOps:** Se enfoca en automatizar la implementación y gestión de la infraestructura y las aplicaciones. También se puede combinar con otras herramientas para diseñar, como las de integración y distribución continuas y las de gestión de la configuración.



   ## Ejemplos de uso de Git Flow


2. **git flow init**: Inicializa un nuevo repositorio Git para usar Gitflow. Esto configura las ramas principales (master y develop) y establece algunas opciones de configuración.
    <br>
3. **git flow feature start [nombre_feature]**: Crea una nueva rama de características basada en la rama develop. Se utiliza para desarrollar nuevas características.
    <br>
4. **git flow feature finish [nombre_feature]**: Fusiona una rama de características terminada de vuelta en la rama develop y la elimina.
    <br>
5. **git flow feature pull origin [nombre_feature]**: Publica una feature por otro usuario. Útil si otro colaborador ha realizado cambios en la rama remota y se desea sincronizar la rama local con los cambios.
    <br>
6. **git flow feature track [nombre_release]**: Se crea una nueva rama basada en la rama develop, permite empezar a trabajar en una nueva característica.
    <br>

7. **git flow release start [nombre_release]**: Crea una nueva rama de lanzamiento basada en la rama develop. Se utiliza para preparar una versión para lanzamiento.
    <br>
8. **git flow release finish [nombre_release]**: Fusiona una rama de lanzamiento terminada en las ramas master y develop, crea una etiqueta de versión y elimina la rama de lanzamiento.
    <br>
9. **git flow hotfix start [nombre_hotfix]**: Crea una nueva rama de hotfix basada en la rama master. Se utiliza para corregir problemas críticos en producción.
    <br>
10. **git flow hotfix finish [nombre_hotfix]**: Fusiona una rama de hotfix terminada en las ramas master y develop, crea una etiqueta de versión y elimina la rama de hotfix.

# Bibliografía


https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow

https://willywes.medium.com/por-qu%C3%A9-es-una-buena-idea-utilizar-gitflow-c92c5e7754e0

https://www.reddit.com/r/git/comments/vnfsr8/desperately_need_help_finding_an_alternative_to/

https://docs.github.com/en/get-started/using-github/github-flow

https://about.gitlab.com/topics/version-control/what-is-gitlab-flow/

https://blog.soyhenry.com/que-es-el-pair-programming/#:~:text=El%20Pair%20Programming%20es%20una,para%20intervenir%20en%20el%20c%C3%B3digo.

https://www.babelgroup.com/es/Media/Blog/Abril-2021/Cinco-Git-Workflows-para-mejores-proyectos


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

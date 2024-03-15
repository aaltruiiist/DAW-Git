## Alternativas a Git Flow

   **1. GitLab Flow:**  Es una alternativa que nace a partir de las carencias que se detectaron en GitHub Flow y Git Flow. 
   El flujo consta de una rama master, ramas features y ramas de entorno; cada vez que se acaba una feature se hace un merge request a master. Cuando la rama master cuenta con varias features, se hace un merge request a preproducción y luego a producción.
   No se necesitan ramas release ya que cada entorno es desplegado con cada merge request aceptada.

   **2. Trunk-based Flow:** Este flujo presenta un cambio de filosofía:
   Los desarrolladores deben colaborar siempre sobre master.
   En casp de que una evolución compleja, se hace uso de features flags para activar o desactivar nuevas características.
   Se prefiere la metodología Pair-Programming (Dos personas trabajando en paralelo sobre el mismo código).

   **3. Master-only Flow:** Este flujo de trabajo usa solo una rama, la cual es infinita. Se realizan features y hot-fix sobre la misma rama y se testean en local con un commit, cuando se aprueba el nuevo cambio se hace un push contra la rama principal y se despliega en producción al instante.



   ## Ejemplos de uso de Git Flow


1. **git flow init**: Inicializa un nuevo repositorio Git para usar Gitflow. Esto configura las ramas principales (master y develop) y establece algunas opciones de configuración.
    <br>
2. **git flow feature start [nombre_feature]**: Crea una nueva rama de características basada en la rama develop. Se utiliza para desarrollar nuevas características.
    <br>
3. **git flow feature finish [nombre_feature]**: Fusiona una rama de características terminada de vuelta en la rama develop y la elimina.
    <br>
4. **git flow feature pull origin [nombre_feature]**: Publica una feature por otro usuario. Útil si otro colaborador ha realizado cambios en la rama remota y se desea sincronizar la rama local con los cambios.
    <br>
5. **git flow feature track [nombre_release]**: Se crea una nueva rama basada en la rama develop, permite empezar a trabajar en una nueva característica.
    <br>

6. **git flow release start [nombre_release]**: Crea una nueva rama de lanzamiento basada en la rama develop. Se utiliza para preparar una versión para lanzamiento.
    <br>
7. **git flow release finish [nombre_release]**: Fusiona una rama de lanzamiento terminada en las ramas master y develop, crea una etiqueta de versión y elimina la rama de lanzamiento.
    <br>
8. **git flow hotfix start [nombre_hotfix]**: Crea una nueva rama de hotfix basada en la rama master. Se utiliza para corregir problemas críticos en producción.
    <br>
9.  **git flow hotfix finish [nombre_hotfix]**: Fusiona una rama de hotfix terminada en las ramas master y develop, crea una etiqueta de versión y elimina la rama de hotfix.
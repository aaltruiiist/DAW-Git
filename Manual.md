# COMANDOS DE GIT

## Comandos básicos de Git

**git init:** Crea un nuevo repositorio local, si no se le especifica una ruta, lo creará en el directorio actual, sinó en la ruta especificada.
    
    git init [nombre del proyecto]

**git clone:** Comando que permite clonar el codigo fuente de la ultima version de un repositorio ya sea remoto o local.

     Remoto: nombredeusuario@host:/ruta/al/repositorio
     Local: /ruta/al/repositorio

**git add:** Sirve para añadir archivos, el siguiente ejemplo añade un archivo txt.

     git add <ejemplo.txt>
    
**git commit:** Crea una instantánea de los cambios actuales y los guarda en el directorio git.

    git commit -m "Mensaje que acompaña al commit"

**git config:**  Se utiliza para establecer la configuracion de usuario, como el email, nombre de usuario y formato

    git config --global user.email ejemplo@ejemplo.com

La propiedad --global configura ese correo para todos los repositorios locales. Por otro lado si necesitas utilizar diferentes correos puedes utilizar el siguiente parametro:
    
    git config --local user.email ejemplo@ejemplo.com
    
**git status:** Muestra la lista de los archivos que se han modificado y que estan preparados o confirmados:

    git status

**git push:** Sirve para confirmar los cambios locales a la rama del repositorio remoto.

    git push origin <nombre de la rama>
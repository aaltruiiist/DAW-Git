# Ejemplo de como se desplegaría

Se necesitaría un servidor de integración continua, configurado para monitorizar el repositorio.

El servidor clona el repositorio en su entorno de ejecución para poder trabajar con los archivos.

Cada vez que se detecta un cambio en el repositorio, el servidor inicia un proceso de construcción. De lo que trata dicho proceso es de ejecutar comandos o scripts para compilar el código fuente y generar archivos ejecutables, paquetes, etc.

Una vez acabado el proceso anterior, se ejecutan pruebas unitarias automatizadas para garantizar el funcionamiento correcto.

Una vez completado, el servidor de integración continua notifoca sobre el resultado de la compilación y las pruebas.

# Explicación del .yml 

El archivo .yml es un archivo de configuración en formato YAML, en el que se especifica como se debe comportar el sistema de integración continua al construir, probar y desplegar el software. Es utilizado para automatizar el proces o de CI.

En el archivo podemos encontrarnos con elementos tales como:
1. jobs: Define los trabajos que se ejecutarán como parte del proceso de integración continua.
2. runs-on: Especificación del sistema operativo en el que se ejecutará.
3. steps: Define los pasos que se ejecutarán.

# Bibliografía

https://docs.gitlab.com/runner/
https://docs.github.com/actions/using-github-hosted-runners/about-github-hosted-runners
https://learn.microsoft.com/en-us/azure/devops/pipelines/agents/agents?view=azure-devops
https://docs.gitlab.com/ee/ci/pipelines/
https://docs.github.com/en/actions/using-workflows
https://learn.microsoft.com/en-us/azure/devops/pipelines/yaml-schema/?view=azure-pipelines
https://es.wikipedia.org/wiki/Integraci%C3%B3n_continua
https://www.atlassian.com/es/agile/software-development/continuous-integration
https://www.atlassian.com/es/continuous-delivery/continuous-integration
https://www.redhat.com/es/topics/automation/what-is-yaml
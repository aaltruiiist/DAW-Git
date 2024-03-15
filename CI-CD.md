# Manual CI-CD

# Indice

- [Manual CI-CD](#manual-ci-cd)
- [Indice](#indice)
- [Runners y Pipelines](#runners-y-pipelines)
- [Para que sirve la integración continua](#para-que-sirve-la-integración-continua)
- [Ejemplo de como se desplegaría](#ejemplo-de-como-se-desplegaría)
- [Explicación del .yml](#explicación-del-yml)
- [Bibliografía](#bibliografía)
  
# Runners y Pipelines
**Runners:** Los runners en integración continua pueden ser máquinas virtuales, contenedores Docker, o incluso dispositivos físicos. Un runner es un agente que ejecuta automáticamente tareas como compilación, pruebas y despliegue según lo definido en un pipeline de CI/CD. Su función es acelerar y automatizar el proceso de desarrollo de software al garantizar la calidad y consistencia del código en cada iteración.
    <br>
**Pipelines:** Los pipelines en integración continua son flujos de trabajo automatizados que definen las etapas y acciones a realizar en cada etapa, como compilación, pruebas y despliegue de software. Se configuran mediante archivos YAML (o similares) en el repositorio de código y se ejecutan automáticamente en respuesta a eventos como pushs de código. Su objetivo es automatizar y estandarizar el proceso de desarrollo, asegurando la consistencia y calidad del software entregado.
    <br>
# Para que sirve la integración continua
La integración continua (CI) implica la integración automática y frecuente de cambios en el código de un proyecto en un repositorio compartido. Detecta errores tempranos y facilita la corrección rápida, manteniendo así la estabilidad del proyecto y permitiendo una colaboración más fluida entre desarrolladores. En resumen, la CI acelera el ciclo de desarrollo al garantizar entregas regulares y confiables, lo que mejora la satisfacción del cliente y la capacidad de adaptación del software al mercado.

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


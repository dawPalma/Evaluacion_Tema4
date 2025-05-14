""# Apuntes sobre Comandos Git
Git es una herramienta de control de versiones distribuido que permite gestionar y registrar los cambios en el código de un proyecto de forma segura y eficiente.

Comandos Básicos:
git init
 Inicializa un nuevo repositorio Git en el directorio actual.

 git init


git add
 Añade archivos al área de preparación (staging area) para ser confirmados en el próximo commit.

 git add archivo.txt


git commit
 Registra los cambios añadidos al área de preparación en el historial de Git.

 git commit -m "Mensaje descriptivo del cambio"


git status
 Muestra el estado de los archivos en el área de trabajo y en el staging.

 git status


git log
 Muestra el historial de commits del repositorio.

 git log



Comandos para Deshacer Cambios:
git restore
 Descarta cambios en el área de trabajo.

 git restore archivo.txt


git reset
 Revierte cambios en el historial de commits (sin eliminar el código):

 git reset --soft HEAD~1  # Revierte el último commit, mantiene los cambios


git revert
 Crea un nuevo commit que deshace los cambios de un commit anterior.

 git revert id_del_commit



Comandos de Visualización de Cambios:
git diff
 Muestra las diferencias entre el área de trabajo y el staging.

 git diff


git diff --staged
 Muestra las diferencias entre el staging y el último commit.

 git diff --staged



Comandos de Ramas (Branches):
git branch
 Muestra todas las ramas del repositorio o crea una nueva si especificas un nombre.

 git branch nombre_de_rama


git checkout
 Permite moverse entre ramas.

 git checkout nombre_de_rama


git switch
 Alternativa moderna a checkout.

 git switch nombre_de_rama


git merge
 Fusiona una rama con la rama actual.

 git merge nombre_de_rama



Comandos para Repositorios Remotos:
git clone
 Clona un repositorio remoto a tu máquina local.

 git clone https://github.com/usuario/repositorio.git


git push
 Sube los cambios del repositorio local al repositorio remoto.

 git push origin main


git pull
 Descarga los cambios del repositorio remoto al local y los fusiona.

 git pull origin main


git fetch
 Descarga los cambios remotos pero no los fusiona.

 git fetch origin main



Etiquetado (Tags):
git tag
 Lista las etiquetas disponibles.

 git tag


git tag -a v1.0 -m "Versión 1.0"
 Crea una nueva etiqueta con un mensaje.

 git tag -a v1.0 -m "Versión 1.0"


git push origin v1.0
 Sube la etiqueta al repositorio remoto.

 git push origin v1.0



Trabajo Colaborativo:
git stash
 Guarda cambios temporalmente sin hacer un commit.

 git stash


git stash pop
 Restaura los cambios guardados con stash.

 git stash pop



Resolución de Conflictos:
Cuando dos ramas modifican el mismo archivo y se intenta fusionar, se produce un conflicto. Para solucionarlo:
Edita los archivos conflictivos.


Una vez solucionados, añade los cambios:

 git add archivo.txt


Finaliza el merge con:

 git commit



Buenas Prácticas:
Realizar commits pequeños y frecuentes.


Escribir mensajes descriptivos en cada commit.


Mantener las ramas organizadas.


Sincronizar regularmente el repositorio local con el remoto.


Evitar hacer force push para no sobreescribir el trabajo de otros.

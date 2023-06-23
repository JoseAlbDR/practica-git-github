# Práctica del módulo Git-GitHub

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
  - git reset --hard HEAD~1
  - Porque primero queremos "deshacer" el ultimo commit y también queremos perder los cambios en el working copy.
  - También podría haber hecho un git reset HEAD~1 y luego un git restore git-nuestro.md, pero opté por usar el modificador --hard

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
  - git reset --hard 01301c9, siendo 01301c9 el short hash del commit al que quiero moverme (obtenido con el comando git reflog).
  - Utilizo el modificador --hard para que el git reset afecte al working copy y recuperar los cambios perdidos en el paso anterior.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
  - No, porque no hay ningun cambio realizado en la rama master (main en mi caso) en el archivo git-nuestro.md, de echo al hacer el merge desde styled no se realiza ningun cambio porque styled ya incluyia todos los cambios realizados en la rama main.
    
- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
  - Sí, porque estamos intentando hacer un merge de dos ramas que han modificado el mismo archivo.
    
- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
  - No, porque desde la rama main no se modificó el archivo git-nuestro.md por lo tanto el merge hace que se apliquen los cambios realizados en la rama styled a la versión del archivo en la rama main.
    
- ¿Qué comando o comandos utilizaste en el paso 25?
  - git graph
    
- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?
  - Sí, porque desde la rama main no se hicieron nuevos commits desde la creacion de la rama title, por lo tanto el merge podria haber sido fast forward (simplemente apuntar con la rama main al mismo commit al que apunta la rama title donde se añadió el título)
    
- ¿Qué comando o comandos utilizaste en el paso 27?
  - git reset HEAD~1
    
- ¿Qué comando o comandos utilizaste en el paso 28?
  - git restore git-nuestro.md
    
- ¿Qué comando o comandos utilizaste en el paso 29?
  - git branch -D title
    
- ¿Qué comando o comandos utilizaste en el paso 30?
  - git reflog para buscar el ultimo commit donde aparecia la rama title
  - git branch title para volver a crear la rama title
  - git checkout title para no estar en detached head (en realidad no era necesario)
  - git checkout main
  - git merge title
    
- ¿Qué comando o comandos usaste en el paso 32?
- - git checkout 21e761f7046196baeb211cb66eafff987f468d7c siendo éste el hash del primer commit donde se crea el archivo
    
- ¿Qué comando o comandos usaste en el punto 33?
  - git reflog para vuscar el commit donde se hacia el merge de main con title (main absorve a title)
  - git checkout 79564c2 siendo éste el hash resumido del merge

Me salté el paso 31 de eliminar el resto de ramas e hice los tags antes de eliminar las ramas por lo tanto al intentar moverme al tag htmlify me decia que era un nombre ambiguo y me movia directamente a la rama htmlify, despues de borrar las ramas si me pude mover al tag htmlify.

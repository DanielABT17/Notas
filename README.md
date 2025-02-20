COMANDOS GIT

git commit --> Guarda los cambios en el repositorio
git branch NombreRama --> Crea una nueva rama
git checkout NombreRama --> Situarce en una rama (Modifica Head)
git merge Rama --> Combina dos ramas
git rebase Rama --> Combina dos ramas de forma secuencial para un log mas claro
git checkout Rama^ --> Te envia posiciona en el padre de la rama
git checkout Rama~n -- Te envia hasta el n padre en esa rama n= numero x
git branch -f main HEAD~3 --> Mueve (forzadamente) la rama main tres padres atrás de HEAD.
git reset HEAD~1(commit) --> revierte los cambios moviendo la referencia de una rama hacia atrás en el tiempo a un commit anterior
git revert (commit) --> revertir cambios y compartir esa revertida con el resto, nuevo commit aplicado sobre el que queríamos revertir este nuevo commit C2' introduce cambios - sólo que esos cambios son exactamente los necesarios para revertir los que introdujo
git cherry-pick <Commit1> <Commit2> <...> --> copiar una serie de commits sobre tu ubicación actual (HEAD)
git rebase -i HEAD~n --> rebase interactivo
git commit --amend --> aplica modificacion hecha con rebase
git tag NombreTag commit --> Poner una marca en un commit
git describe -->  saber dónde estás después de que te hayas movido varios commits hacia adelante o atrás en la historia
<tag>_<numCommits>_g<hash>
Donde tag es el tag más cercano en la historia, numCommits dice a cuántos commits de ese tag estás, y <hash> es el hash del commit que estás describiendo.

git clone --> crear copias locales de un repositorio remoto
git fetch --> Traer datos desde un repositorio remoto

git fakeTeanwork 3 // simular commits remotos
git push --> es el responsable de subir tus cambios a un remoto específico

git fetch; git rebase o/main; git push
Actualizamos nuestra representación local del remoto con git fetch, rebaseamos nuestro trabajo para reflejar los nuevos cambios del remoto, y después los pusheamos con git push.

git fetch; git merge o/main; git push
Actualizamos nuestra representación local del remoto usando git fetch, mergeamos el nuevo trabajo junto con el nuestro (para reflejar los nuevos cambios en el remoto), y después los pusheamos usando git push.

lo mismo con git pull --rebase; git push
lo mismo git pull; git push

git fetch origin foo

Git va a ir a la rama foo en el remoto, va a traer todos los commits que no estén presentes localmente, y luego los aplicará sobre la rama o/foo localmente.

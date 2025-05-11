# Diff - Log - Ver - Mostrar

---

`git diff`: muestra los cambios hechos entre lo stageado/indexado/trackeado y lo que no fue agregado (working tree). Osea muestra lo que podés AGREGAR al index para posteriormente commitear.

`git diff --cached`: muestra los cambios ya stageados/indexados/cacheados con respecto al último commit. Se le puede pasar el id del commit al final para comparar con un commit específico.

`git diff <commit>`: muestra los cambios de tu index/working tree (no stageado/no cacheado) con un commit. Se puede usar HEAD para comprarlos con el ultimo commit o un nombre de rama para compararlo con la punta de esa rama (último commit de esa rama)..

`git diff rama1 rama2`: muestra diferencias entre esas ramas.

# Mostrar 

---

`git ls-tree --full-tree -r --name-only HEAD`: mostrar archivos comiteados siendo trackeados actualmente 

`git check-ignore *`: desde la carpeta deseada chequear si los archivos son activamente ignorados.

(source: https://scriptcrunch.com/git-show-ignored-files/)


`git log --name-status HEAD^..HEAD`: Para ver que se comiteo en el ultimo <br><br>

`git log -1`, `git show`, `git diff`: devuelven un resultaodo similar al comando de arriba.

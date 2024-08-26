## Branches

source: https://www.youtube.com/watch?v=pDmYNK68IEc

Cuando creás una nueva rama se copian todos los archivos del ultimo commit del master. Si luego de eso se pushean nuevos commits al master, la nueva rama NO los tendrá. De la misma manera, todos los commits que se hagan en la nueva rama NO aparecerán en la rama master.<br><br>


`git branch nuevaRama`: crear nueva branch

`git branch --list`: chequear lista de ramas, la que tiene un * es en la que estamos parados.


`git checkout nuevaRama`: para cambiar de rama hacia la nuevaRama.


`git checkout -b nuevaRama2`: crea rama y se mueve hacia ella en un paso, para no hacer los dos pasos anteriores

Luego crea archivos dentro de esa rama, los pasa a staging ("add .") y los commitea (commit -m "mensaje")

Hasta ahora la nuevaRama2 está creada en el entorno local, si intentamos pushear nos va a tirar error

fatal: current branch nuevaRama2 has no upstream branch. To push the current branch and set the remote upstream, use `git push --set-upstream origin nuevaRama2`

Se puede crear la rama directamente en GitHub o usar el código que nos recomienda Git en la consola. Se ejecuta el código y ahora en el repo de GitHub aparece una nueva rama nueva. 

https://www.youtube.com/watch?v=sSD9jroO53Y&list=PLriKzYyLb28nCh3jJLROcYBvj7ZO0l-3G&index=5

## Merge
<br>


`git checkout master`: Para mergear primero hay que cambiar a la rama master.


`git merge nuevaRama2`: para hacer el merge, se abre el editor Vim para escribr el commit del merge , tipeamos :q y enter para salir.

`git add .`
`git commit -m "Se mergeó la rama nuevaRama2 a master"`

La consola dice "Your branch is ahead of origin/master by 2 commits. Use git push to publick your local commits", quiere decir que en el entorno local la rama master esta 2 commits adelantada de origin/master, osea el origen remoto (GitHub), la rama master.<br><br>
`git push`

Ahora se puede eliminar la rama nuevaRama2 ya que ya fue mergeada. La elimina del entorno LOCAL

`git branch -d nuevaRama2`

Si nos fijamos en GitHub, sigue figurando la rama nuevaRama2. Para borrarla se puede hacer desde GitHub o por consola (ojo cuando la eliminas directamente de GitHub sigue figuran en el entorno local y viceversa).

`git push origin :nuevaRama2`

## Comandos varios

`git clone -b <branch-name> <repo-url>` : clona una rama específica desde un repositorio remoto. 












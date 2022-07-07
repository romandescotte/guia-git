## Pull request

<br>

El pull request es un pedido de mergear dos ramas. Puede ser con la rama main/master u otra.

Se crea una rama, se comitean los cambios, se pushea a la nueva rama, se crea el pull request.

Si luego de creado el PR tengo mas commits los puedo comitear y pushear que se van a agrupar en el mismo PR.

En Github desktop:

Create new branch (bring my changes to "nuevaRama")
Publish Branch

Luego en GitHub.com: Compare & pull request. Chequear que el repo al que le solicitemos el pull request sea el nuestro, no el upstream del cual forkeamos.

Tipos de merge:

Merge commit: crea un commit de tipo merge que agrupa todos los commits del PR.

Squash and merge: combina los commits en uno solo y lo pone en la nueva rama.

Rebase and merge: se ponen los commits por separado, en orden, arriba del ultimo commit.  <br><br>

--------
<br><br>

## GitHub CLI:<br><br>

`gh pr list`: lista los PR abiertos<br><br>

`gh pr list -s "all" | "closed"`: lista todos los PR con ese estado (--state).<br><br>

`gh pr list --assignee "userName"`<br><br>

`gh pr status`<br><br>

`gh pr list --label "bug"`<br><br>

`gh pr view "14": abre el PR en el browser` <br><br>

`git checkout -b "nuevaRama"`<br><br>

`gh pr create -t "Sample Title" -b "Sample Body": crea el PR en la rama actual`<br><br>












# stash unstash

---

`git stash <mensaje>`: Guarda en el stash los cambios presentes en el INDEX (aparte, como si fuera antes del working tree, similar a borradores). Osea que para stashear, primero hay que trackearlos (agregarlos al index/staging area). El mensaje es opcional

`git stash list`: lista las entradas de borradores que hay. (stash@{0} es la ultima entrada )

`git stash show`: muestra los cambios como una diferencia entre el borrador (stash) y el commit en el momento en que se stasheo.

`git stash pop <stash>`: remueve el stash de la papelera y lo aplica sobre el estado actual del working tree. El working tree debe matchear el index

`git stash clear`: para remover todas las entradas de borradores.



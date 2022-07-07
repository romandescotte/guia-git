# Iniciar un repositorio desde 0
<br>

## Estados de git:
<br>

Working Directory/working tree (LOCAL)<br>
|<br>
|<br>
Index/Staging Area/Current directory cache/Staged files/Caché (LOCAL) <br>
|<br>
|<br>
Repository (LOCAL) <br>
|<br>
| <br>
Remote
<br><br>
(source: https://ndpsoftware.com/git-cheatsheet.html#loc=index;)
<br><br>

## Comandos básicos

<br>
Para abrir la pagina con el manual:<br><br>

`git help <command>`<br><br>
`git help`<br><br>
`git help -a`<br><br>
`git help -g`<br><br>

`git init`: inicia el repo local (working directory) en la carpeta en la que se ejecute. Crea la carpeta oculta .git. Se ejecuta una vez por proyecto. En VS Code se pintan los archivos de color verde (aparece una U de untracked)<br><br>

`git status`: muestra el estado del working directory, con -s ó --short  nos indica en una línea el estado de los archivos
. Aparecen con el símbolo ?? los archivos sin trackear. Los archivos agregados aparecen con una "A" verde (added). Los que fueron añadidos Y modificados aparecen con "AM". Hasta ahora los archivos estan en el working directory.<br><br>



`git add <file>`: agrega el archivo sin trackear al Index/Staging Area<br><br>


`git add .`: agrega todos los archivos sin trackear<br><br>

Si hacemos modificaciones al archivo mientras está en el staging area aparece una linea amarilla en VS Code (modificado) o una linea cyan (nuevo) y una 'M' a la izquierda del nombre del archivo.<br><br>

`git status -u`: comprobar los cambios en git(untracked)<br><br>
`git status -v`: muestra las lineas modificadas que no estan añadidas al index (en rojo y verde).<br><br>

`git add -u`: actualizar esos cambios ejecutar<br>

o 

`git add 'nombredearchivo.txt'`<br><br>

 
`git commit`: agrega los archivos al repo LOCAL, abre el editor VIM.<br><br>

`git commit -m "titulo del commit"`: agrega los archivos al repo LOCAL sin abrir el editor VIM- Ees el primer snapshot del codigo acompañado de un mensaje log que describe esos cambios<br><br>


`git commit -am "titulo del commit"`: agrega al staging (los archivos presentes en el ultimo commit) y commitea al mismo tiempo<br><br>

En el editor vim para poder tipear hay que presionar "i", luego "Esc" para dejar de editar y ":wq" y "Enter" para escribir los cambios y salir.<br><br>

`git log --oneline`: arroja el historial de commits en una linea.<br><br>

`git reset --hard [commitID]`: vuelve el codigo al commit especificado. se puede volver hacia adelante nuevamente siempre especificando el commitID. OJO creo que deshace los cambios hechos a los archivos<br><br>

Creamos un repo remoto desde GitHub. Primer comando para agregar el linkeo al repo remoto:<br><br>

`git remote add origin https://github.com/sk8mumy/NOMBRE-DEL-REPO.git`  origin es el alias de la URL<br><br>


`git branch -M main`: cambia el nombre de la rama a main (-M es igual a --move --force. Segun documentacion permite renombrar la 
//rama aunque exista previamente file:///C:/Program%20Files/Git/mingw64/share/doc/git-doc/git-branch.html.<br><br>


`git push -u origin main`: -u es lo mismo que --set-upstream, "For every branch that is up to date or successfully pushed, add upstream (tracking) reference," <br><br>

`git pull` : para traerte los cambios desde el servidor<br><br>

`git clone`: clona el repositorio del servidor al disco duro<br><br>
`git log`: muestra el registro de commits hechos<br><br>
`git ls-files`: lista los archivos comiteados<br><br>
`git rm --cached "nombre de archivo"`: untrackea ese archivo
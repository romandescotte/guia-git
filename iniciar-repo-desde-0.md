# Iniciar un repositorio desde 0

---

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

<br>

# Clonar desde git bash

----------

<br>

> **Lo mejor es forkearlo primero en GitHub y luego clonar el repo con el link del fork. (aparece "forked from..." en nuestro repo y te ahorras el paso de setear el origin).**
<br>

Estos son los pasos para forkear un repo, lo mismo que en clase-9-resumen (r/argentina-programa), solo que con Git Bash.<br><br> 

`git clone https://github.com/r-argentina-programa/introduccion-a-js` <br><br>

`git remote -v`<br><br>

```
origin  https://github.com/r-argentina-programa/introduccion-a-js (fetch)
origin  https://github.com/r-argentina-programa/introduccion-a-js (push)
```
<br>
Esos son los origenes remotos del repo clonado, ahora vamos a borrarlos y crear nuevos, ya que no puedo pushear nada nuevo al repo original (yo no soy su autor, no tengo permisos)<br><br>

`git remote remove origin`<br><br>

`git remote -v`<br>

no muestra ningun origen<br><br><br>

Ahora creo un repo en GitHub con nombre "prueba"


`git remote add ble https://github.com/sk8mumy/prueba`<br><br>

ble es el alias para el origen remoto.<br><br>

`git remote -v`<br><br>
```
ble     https://github.com/sk8mumy/prueba (fetch)
ble     https://github.com/sk8mumy/prueba (push)
```
<br><br>
`git remote rename ble origin`

cambio el nombre

`git remote -v`
<br><br>

```
origin  https://github.com/sk8mumy/prueba (fetch)
origin  https://github.com/sk8mumy/prueba (push)

```


esta ok<br><br>

`git push origin`<br><br>

`git push --set-upstream origin master`<br><br>

`git push --set-upstream origin master`<br><br>

```
Enumerating objects: 185, done.
Counting objects: 100% (185/185), done.
Delta compression using up to 4 threads
Compressing objects: 100% (92/92), done.
Writing objects: 100% (185/185), 290.09 KiB | 26.37 MiB/s, done.
Total 185 (delta 83), reused 185 (delta 83), pack-reused 0
remote: Resolving deltas: 100% (83/83), done.
To https://github.com/sk8mumy/prueba
 * [new branch]      master -> master
Branch 'master' set up to track remote branch 'master' from 'origin'.
```

<br>
Voy a GitHub, actualizo y veo el repo ya subido PERO no dice Forked from r/argentina-programa.

<br>

## Fork desde GH Command Line

Con Github desktop instalado probar:

`gh --help`

`gh auth login --web`

`gh repo fork <repository_url> --clone`


Para fetchear nuevos cambios a nuestro fork desde el repo original (upstream) se puede ir a GitHub y tocar en el boton "Fetch upstream".

o

`git remote -v `

`git remote add upstream <URL_fork_original>`
 










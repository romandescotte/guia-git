## Rebase explicado

Desde la rama actual en la que estás parado te traés los cambios de la rama que especifiques como argumento en el comando. Ejemplo:

Estando parado en master ejecuto: `git rebase arreglaBug`. Me trae a master los commits hechos en la rama arreglaBug.

## Rebase para gh-pages
<br>

`git add .` 
<br><br>
`git status`: to see what changes are going to be commited
<br><br>
`git commit -m 'Some descriptive commit message'`
<br><br>
`git push origin master` 
<br><br>
`git checkout gh-pages`: go to the gh-pages branch
<br><br>
`git rebase master`: bring gh-pages up to date with master 
<br><br>
`git push origin gh-pages`: commit the changes
<br><br>
`git checkout master `: return to the master branch




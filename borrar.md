## Borrar repo local (de 0)<br>
<br>

OJO ESTO BORRA SIN PASAR PO LA PAPELERA, DEFINITIVAMENTE !!! `rm -rf .git`: to avoid endless prompts (and force the command recursively)

`rm -rf .git*` : to delete .gitignore and .gitmodules if any
Then from the same ex-repository folder, to see if hidden folder .git is still there:

`ls -lah` : lists every file

## Borrar origen remoto

source: https://scriptcrunch.com/git-show-ignored-files/
<br><br>

`git remote rm origin`: borra el origen remoto

`git remote -v`: muestra origenes

`git remote show <alias>`: muestra informacion acerca de ese origen

`git remote add origin <URL>` : agregar fuente remota


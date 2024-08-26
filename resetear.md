## Reset

<br>

`git log --name-status HEAD^..HEAD`: Para ver que se comiteo en el ultimo <br><br>

as noted by other folks in this question, you can use git log -1, git show, and git diff to get the same sort of output



`git reset --soft HEAD^`: Para descomitear. Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed", as git status would put it. No revierte los cambios hechos a los archivos, solo los descomitea.
<br><br>
Luego para sacar del staging area:
<br><br>

`git restore --staged path/to/unwanted_file`<br><br>


`git commit -c ORIG_HEAD`: para commitear nuevamente usando el mismo mensaje, titulo y abriendo el editor de texto (-c).


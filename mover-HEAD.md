# mover el HEAD

----

`git checkout <commit>`: podes volver a pararte sobre el commit especificado. Guarda el commit desde donde venís. Git advierte:  
>You are in 'detached HEAD' state. You can look around, make experimental 
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.      
If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command.  
Example:  
git switch -c <'new-branch-name'>  
Or undo this operation with:  
git switch -

`git checkout main`: volver al commit original. No es necesario poner el id del commit en este caso.

fuente: https://stackoverflow.com/questions/4114095/how-do-i-revert-a-git-repository-to-a-previous-commit
# Reset
---
<br>

`git reset <'modo'> <'commit'>`: resetea el head de la rama al commit especificado. Dependiendo qué  modo se use reseteará o no el index y/o el working tree.  

`git reset --soft HEAD^`: Para descomitear. Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed", as git status would put it. No revierte los cambios hechos a los archivos, solo los descomitea.
<br>

Luego:

`git restore --staged path/to/unwanted_file`: para remover archivo del staging area

`git reset path/to/unwanted_file`: es lo mismo que el comando de arriba.

`git commit -c ORIG_HEAD`: para commitear nuevamente usando el mismo mensaje, titulo y abriendo el editor de texto (-c).

Fuente: https://git-scm.com/docs/git-reset


--soft
Does not touch the index file or the working tree at all (but resets the head to <commit>, just like all modes do). This leaves all your changed files "Changes to be committed", as git status would put it.

--mixed
Resets the index but not the working tree (i.e., the changed files are preserved but not marked for commit) and reports what has not been updated. This is the default action.

If -N is specified, removed paths are marked as intent-to-add (see git-add[1]).

--hard
Resets the index and working tree. Any changes to tracked files in the working tree since <commit> are discarded. Any untracked files or directories in the way of writing any tracked files are simply deleted.

--merge
Resets the index and updates the files in the working tree that are different between <commit> and HEAD, but keeps those which are different between the index and working tree (i.e. which have changes which have not been added). If a file that is different between <commit> and the index has unstaged changes, reset is aborted.

In other words, --merge does something like a git read-tree -u -m <commit>, but carries forward unmerged index entries.

--keep
Resets index entries and updates files in the working tree that are different between <commit> and HEAD. If a file that is different between <commit> and HEAD has local changes, reset is aborted.

--[no-]recurse-submodules
When the working tree is updated, using --recurse-submodules will also recursively reset the working tree of all active submodules according to the commit recorded in the superproject, also setting the submodules' HEAD to be detached at that commit.

See "Reset, restore and revert" in git[1] for the differences between the three commands.

OPTIONS
-q
--quiet
Be quiet, only report errors.

--refresh
--no-refresh
Refresh the index after a mixed reset. Enabled by default.

--pathspec-from-file=<file>
Pathspec is passed in <file> instead of commandline args. If <file> is exactly - then standard input is used. Pathspec elements are separated by LF or CR/LF. Pathspec elements can be quoted as explained for the configuration variable core.quotePath (see git-config[1]). See also --pathspec-file-nul and global --literal-pathspecs.

--pathspec-file-nul
Only meaningful with --pathspec-from-file. Pathspec elements are separated with NUL character and all other characters are taken literally (including newlines and quotes).

--
Do not interpret any more arguments as options.

<pathspec>…​
Limits the paths affected by the operation.

For more details, see the pathspec entry in gitglossary[7].
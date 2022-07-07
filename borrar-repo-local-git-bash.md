## Borrar repo local (de 0)<br>
<br>

`rm -rf .git`: to avoid endless prompts (and force the command recursively)

`rm -rf .git*` : to delete .gitignore and .gitmodules if any
Then from the same ex-repository folder, to see if hidden folder .git is still there:

`ls -lah` : lists every file
Si me confundi y lo pushee:

`git rm --cached archivo-sensible.txt`

Agrego archivo-sensible.txt al .gitignore

`git add .gitignore`

`git commit -m "agrega archivo-sensible.txt al .gitignore"`
`git push`

Ahora no figura mas en el repo remoto.

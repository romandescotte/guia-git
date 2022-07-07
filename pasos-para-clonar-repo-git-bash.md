## Clonar desde git bash
----------
<br>

Lo mejor es forkearlo primero en GitHub y luego clonar el repo con el link del fork. (aparece "forked from..." en nuestro repo y te ahorras el paso de setear el origin).<br><br>

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












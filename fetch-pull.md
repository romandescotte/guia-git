# Fetch/Pull

---

Cuando intentamos pushear al repositorio remoto y éste está adelantado de nosotros, Git tira error:  

```Updated were rejected because the remote contains work that you don't have locally.This is usually caused by another repository pushing to the same ref. You may want to first integrate the remote changes (e.g., 'git pull ...') before pushing again.``` 

Si alguien crea una rama nueva en el remoto y nosotros no la tenemos en el local, no podemos  crear una rama con ese mismo nombre ni pushear ni pullear hacia ella, primero tenemos que fetchearla

`git fetch origin`: para traer los cambios desde el origin/master (remoto)

`git log origin/master ^master`: para ver diferencias entre el local y el remoto.

`git checkout Contact`

`git fetch origin nombrederama:nombrederama`: Si queremos fetchear solo una rama en particular.
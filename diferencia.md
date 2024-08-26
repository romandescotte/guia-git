# Diff

---

`git diff`: muestra los cambios hechos entre lo stageado/indexado/trackeado y lo que no fue agregado (working tree). Osea muestra lo que podés AGREGAR al index para posteriormente commitear.

`git diff --cached`: muestra los cambios ya stageados/indexados/cacheados con respecto al último commit. Se le puede pasar el id del commit al final para comparar con un commit específico.

`git diff <commit>`: muestra los cambios de tu index/working tree (no stageado/no cacheado) con un commit. Se puede usar HEAD para comprarlos con el ultimo commit o un nombre de rama para compararlo con la punta de esa rama (último commit de esa rama)..



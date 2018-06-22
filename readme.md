#¿Qué comando utilizaste en el paso 11? ¿Por qué?

* git reset --hard HEAD~1

Uso este comando para retroceder al commit anterior con HEAD~1 y con --hard para que
modifique mi working copy.

#¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

Podemos realizarlo de distintas maneras he optado por la siguiente.

* git reflog

edcd436 HEAD@{0}: reset: moving to HEAD~1
c660e25 HEAD@{1}: commit: Modifico git-nuestro.md rama styled
edcd436 HEAD@{2}: checkout: moving from master to styled
edcd436 HEAD@{3}: commit (initial): Creo git-nuestro.md rama master


* git reset --hard c660e25

Utilizo el --hard para la modificacion del working copy y fab9549 para posicionarnos
en ese commit.

#El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

* git branch

Para ver en que rama estoy

* git checkout style 

Para posicionarme en la branch que absorbe a master.

* git merge master
**Already up-to-date.**

No se causa conflicto porque quedamos con los cambios realizados en el último commit que son los realizados en el punto 9 en la rama syled y la rama master esta en el commit padre. por lo que desde Styled tiene acceso a la rama master.

#El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
* git checkout styled
* git branch
* git merge htmlify

Si, porque el archivo git-master.md ha sido cambiado en las mismas lineas en ambas ramas.

#El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No se produce ningún conflicto al ser Fast-Fordward solo adelantamos el puntero master ya que es una lista de commits.

#¿Qué comando o comandos utilizaste en el paso 25?

* git log --graph --decorate --pretty=online

#El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si, ya que sigue siendo una lista de commits y no perdemos acceso a los commits anteriores, igual que en el paso 21. Solo avanzaria el puntero master al commit donde esta el puntero title.

#¿Qué comando o comandos utilizaste en el paso 27?
Se puede realizar de distintas formas yo utilice este.

* git reset HEAD~1

#¿Qué comando o comandos utilizaste en el paso 28?

* git checkout -- git-nuestro.md
 
#¿Qué comando o comandos utilizaste en el paso 29?

* git branch -D title

#¿Qué comando o comandos utilizaste en el paso 30?

* git reflog 
 - localizamos el HASH, donde realizamos el commit del merge de las dos ramas.
* git reset --hard a958dde
 - --hard, para cambiar el working copy y recuperar la modificacion

#¿Qué comando o comandos usaste en el paso 32?

*  git reflog
  - Para localizar el Hash del primer commit donde creamos el git-nuestro.md
* git checkout edcd436
  - Movemos el HEAD al primer commit.

#¿Qué comando o comandos usaste en el punto 33?

* git checkout master
  - Movemos el HEAD al puntero master que estaba en el último commit.
  
César Fernández Nieto

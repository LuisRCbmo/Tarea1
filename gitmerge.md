# Diferencia entre git merge y git merge --no --ff

El comando a tratar es
~~~ 
git merge
~~~
sirve para integrar los cambios de una "rama" a la rama que se encuentre em el momento, creando un nuevo commit con los cambios mezclados

Existe una variante la cual es:
~~~
git merfe --no-ff
~~~
el indicador `--no-ff` evita que `git merge` ejecute un avance rapido , un avance rapido o "fast forward" se da en casos similares al siguiente.

De la rama master se crea una nueva rama llamada "R", una vez se trabaje y se hagan las modificaciones en R se la integrara a la rama master, en esta ocasion. dentro la rama master el ultimo commit registrado fue realizado antes de la creacion de R, por lo tanto una vez echo el `git merge` la rama master apuntara al head de la rama R y mantendra el commit previo a esta, a esto se le llama avanze rapido.

La instruccion `--no-ff` evita el avance rapido y se encarga de que se registre un nuevo commit cuando la rama R se integre a la rama master, asi la rama master tambien modificara su cabezera o head.
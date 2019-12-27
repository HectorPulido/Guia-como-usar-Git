# COMO USAR GIT: TUTORIAL COMPLETO
Los programadores tenemos una relacion amor odio con git, sabemos que es super util pero no sabemos sacar todo el provecho que la herramienta ofrece, asi que si nos obligan solemos usarlo de la forma mas insulsa y aburrida posible...

## GLOSARIO
* <b>ORIGIN:</b> La nube, en nuestro caso el repositorio en github, tambien puede estar en gitlab o bitbucket.
* <b>COMMIT:</b> Punto en el tiempo al cual podemos retroceder de manera sencilla.
* <b>BRANCH:</b> o rama, espacio seguro en donde podemos escribir codigo sin afectar a la rama principal.
* <b>MASTER:</b> Rama o branch principal, usualmente usada para releases a produccion.
## COMANDOS BASICOS
* <b>">>git status"</b> nos da informacion util sobre el repositorio, cambios que hemos hecho, cambios que se van a subir al commit, y nombre de la rama.
* <b>">>git log"</b> nos muestran todos los commits que se han hecho junto con su codigo unico, la fecha y el autor.
## FLUJO NORMAL
1. Primero usar el comando 
">>git add ..." donde los ... representan los archivos a subir, podemos saber que archivos son usando el ">>git status"
2. Crear el commit con el comando 
">>git commit -m '...'" donde los ... representan el nombre del commit. 
3. Subir el commit con el comando 
">>git push origin master" 
## RAMAS
* Para ver nuestras ramas usamos el comando
">>git branch", esto nos muestra que ramas hemos utilizado y en que rama estamos.
* Para crear una rama podemos usar el commando.
">>git branch ..." donde los ... son el nombre de la rama
* Para movernos, usamos el comando.
">>git checkout ..." donde los ... otra vez, son el nombre de la rama.
* Recordad siempre usar pull request para mezclar las ramas.
* Recordad siempre hacer pull antes de crear una rama y crear siempre la rama desde master, no desde otra rama a menos que sepas lo que estas haciendo.
* Las ramas contienen todos los commits de la rama desde la que fue creada hasta el momento de su creacion.
* Para crear una rama y de inmediato moverte a ella en un solo comando puedes utilizar el comando de ">>git checkout -b '...'" donde ... es el nombre de la rama.

## TODO: 
1. Tema de conflictos
2. Video de youtube
3. Solucion de erratas
4. Como instalar git 
5. Traduccion al ingles

# COMO USAR GIT: TUTORIAL COMPLETO
Los programadores tenemos una relacion amor odio con git, sabemos que es super util pero no sabemos sacar todo el provecho que la herramienta ofrece, asi que si nos obligan solemos usarlo de la forma mas insulsa y aburrida posible...

## GLOSARIO
* <b>ORIGIN:</b> La nube, en nuestro caso el repositorio en github, tambien puede estar en gitlab o bitbucket.
* <b>COMMIT:</b> Punto en el tiempo al cual podemos retroceder de manera sencilla.
* <b>BRANCH:</b> o rama, espacio seguro en donde podemos escribir codigo sin afectar a la rama principal.
* <b>MASTER:</b> Rama o branch principal, usualmente usada para releases a produccion.
## COMO INSTALAR GIT
### WINDOWS
Descargar e instalar de el lugar oficial.</br>
https://git-scm.com/download/win </br>
Luego de eso solo utilizar los comandos de git desde el bash de git, desde cmd o desde powershell.
### MAC
En caso de tener Homebrew instalado simplemente usar el comando  </br>
">>brew install git"
De lo contrario descargar de la pagina oficial. </br>
https://brew.sh/ </br>
### LINUX
#### CENTOS / REDHAT
">>sudo yum install git"
#### UBUNTU
">>sudo apt-get install git"
#### FEDORA
">>sudo yum install git-core"

## COMANDOS BASICOS
* <b>">>git status"</b> nos da informacion util sobre el repositorio, cambios que hemos hecho, cambios que se van a subir al commit, y nombre de la rama.
* <b>">>git log"</b> nos muestran todos los commits que se han hecho junto con su codigo unico, la fecha y el autor.
* <b>">>git pull"</b> descarga de la nube todos los datos de la rama actual, ademas descarga todas las ramas.
## FLUJO NORMAL
1. Primero usar el comando 
">>git add ..." donde los ... representan los archivos a subir, podemos saber que archivos son usando el ">>git status"
2. Crear el commit con el comando 
">>git commit -m '...'" donde los ... representan el nombre del commit. 
3. Subir el commit con el comando 
">>git push origin master" 
## RAMAS
Se trata de un espacio seguro en donde podemos escribir codigo sin afectar a la rama principal. git tiene forma de Arbol, siendo la rama principal o tronco la <b>rama master</b> cada rama puede ser ramificada en otras ramas que luego pueden juntarse. Cada rama tiene los mismos commits que su rama padre hasta el momento de crearla, luego de eso los commits no se comparten entre ramas a menos que se haga un merge o un pull request.
* Para ver nuestras ramas usamos el comando
">>git branch", esto nos muestra que ramas hemos utilizado y en que rama estamos.
* Recordad siempre usar pull request para mezclar las ramas.
* Recordad siempre hacer pull antes de crear una rama y crear siempre la rama desde master, no desde otra rama a menos que sepas lo que estas haciendo.
* Las ramas contienen todos los commits de la rama desde la que fue creada hasta el momento de su creacion.
### Crear ramas y movernos entre ellas
* Para crear una rama podemos usar el commando.
">>git branch ..." donde los ... son el nombre de la rama
* Para movernos, usamos el comando.
">>git checkout ..." donde los ... otra vez, son el nombre de la rama.
* <b>TIP:</b> para crear una rama y de inmediato moverte a ella en un solo comando puedes utilizar el comando de ">>git checkout -b '...'" donde ... es el nombre de la rama.
## CONFLICTOS
Si dos desarrolladores modifican a la vez un mismo archivo en las mismas lineas, al momento de juntar los cambios git no sabra que hacer y dara paso a que los desarrolladores sean quienes solucionen el dichoso conflicto.
### Razones para que se de un conflicto
* Al momento de juntar dos ramas en donde el mismo archivo y las mismas lineas hayan sido modificadas.
* Si se hace un ">>git stash" con un archivo modificado y luego se modifica el archivo, al momento de hacer ">>git stash pop" este archivo dara lugar a un conflicto.
* Si un desarrollador esta modificando un archivo en una rama y esa misma rama tiene un commit que no ha sido descargada por el desarrollador al momento de hacer "push" habra un conflicto en caso de que ese archivo haya sido modificado en los commits no descargados. 
### Resolver conflictos
1. Si el conflicto sale de manera expontanea saltar al paso #7
2. Pasarse a master con el comando ">>git checkout master"
3. Descargar la master ">>git pull origin master"
4. Volver a la rama del conflicto con ">>git checkout ..."
5. Hacer merge de la rama normal con master ">>git merge master"
6. Al revisar el resultado del merge veremos algo como "CONFLICT (content): Merge conflict in..."
7. Al momento de revisar el archivo veremos algo como esto:
```
<<<<<<< Updated upstream
hola mundo 456 
=======
hola mundo 123
>>>>>>> Stashed changes
```
Se ve claramente la separacion entre los dos cambios. </br>
8. Para solucionar el conflicto solo hay que deshacerse de los separadores, obviamente estoy hay que hacerlo de manera que el codigo funcione correctamente, **esta es la parte dificil de la resolucon de conflictos y hay que hacerla con mucho tacto**.</br>
9. Luego de solucionar el conflicto hacer el **flujo normal** osea git add, commit, push.</br>
10. Por ultimo hacer de nuevo el pull request, el merge o lo que se estaba realizando.

## TODO: 
* ~~Tema de conflictos~~
* ~~Como instalar git~~
* Solucion de erratas
* Video de youtube
* Traduccion al ingles

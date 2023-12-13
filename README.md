# COMO USAR GIT: TUTORIAL COMPLETO
[![Video sobre como funciona git](https://img.youtube.com/vi/rJRq7U95o8s/0.jpg)](https://www.youtube.com/watch?v=rJRq7U95o8s)

Los programadores tenemos una relación de amor odio con git, sabemos que es superútil, pero no sabemos sacar todo el provecho que la herramienta ofrece, así que si nos obligan solemos usarlo de la forma más insulsa y aburrida posible...

## GLOSARIO
* <b>ORIGIN:</b> La nube, en nuestro caso el repositorio en github, también puede estar en gitlab o bitbucket.
* <b>COMMIT:</b> Punto en el tiempo al cual podemos retroceder de manera sencilla.
* <b>BRANCH:</b> o rama, espacio seguro en donde podemos escribir codigo sin afectar a la rama principal.
* <b>MASTER:</b> Rama o branch principal, usualmente empleada para releases a producción.

## COMO INSTALAR GIT

### WINDOWS
Descargar e instalar del lugar oficial.</br>
https://git-scm.com/download/win </br>
Luego de eso solo utilizar los comandos de git desde el bash de git, desde cmd o desde powershell.

### MAC
En caso de tener Homebrew instalado simplemente utilizar el comando  </br>
">>brew install git"
De lo contrario descargar de la página oficial. </br>
https://brew.sh/ </br>
### LINUX
#### CENTOS / REDHAT
">>sudo yum install git"
#### UBUNTU
">>sudo apt-get install git"
#### FEDORA
">>sudo yum install git-core"

## COMANDOS BASICOS
* <b>">>git status"</b> nos da información útil sobre el repositorio, cambios que hemos hecho, cambios que se van a subir al commit, y nombre de la rama.
* <b>">>git log"</b> nos muestran todos los commits que se han hecho junto con su código único, la fecha y el autor.
* <b>">>git pull"</b> descarga de la nube todos los datos de la rama actual, además descarga todas las ramas.
## FLUJO NORMAL
1. Primero usar el comando 
">>git add <...>" Donde los <...> Representan los archivos a subir, podemos saber que archivos son usando el ">>git status"
2. Crear el commit con el comando 
">>git commit -m '<...>'" Donde los <...> representan el nombre del commit. 
3. Subir el commit con el comando 
">>git push origin <...>" Donde los <...> representan el nombre de la rama donde estás, inicialmente master. 

## RAMAS

Se trata de un espacio seguro en donde podemos escribir código sin afectar a la rama principal. Git tiene forma de Arbol, siendo la rama principal o tronco la <b>rama master</b> cada rama puede ser ramificada en otras ramas que luego pueden juntarse. 

Cada rama tiene los mismos commits que su rama padre hasta el momento de generarla, luego de eso los commits no se comparten entre ramas a menos que se haga un merge o un pull request.
* Para ver nuestras ramas usamos el comando
">>git branch", esto nos muestra que ramas hemos utilizado y en que rama estamos.
* Recordad siempre usar pull request para mezclar las ramas.
* Recordad siempre hacer pull antes de crear una rama y crear siempre la rama desde master, no desde otra rama a menos que sepas lo que estás haciendo.
* Las ramas contienen todos los commits de la rama desde la que fue creada hasta el momento de su creacion.


### Generar ramas y movernos entre ellas
* Para generar una rama podemos emplear el commando.
">>git branch <...>" Donde los  <...> son el nombre de la rama
* Para movernos, usamos el comando.
">>git checkout <...>" donde los <...> otra vez, son el nombre de la rama.
* <b>TIP:</b> para crear una rama y de inmediato moverte a ella en un solo comando puedes utilizar el comando de ">>git checkout -b '<...>'" donde <...> es el nombre de la rama.

## CONFLICTOS
Si dos desarrolladores modifican a la vez un mismo archivo en las mismas líneas, al momento de juntar los cambios git no va a saber que hacer y dará paso a que los desarrolladores sean quienes solucionen el dichoso conflicto.

### Razones para qué sé de un conflicto
* Al momento de juntar dos ramas en donde el mismo archivo y las mismas líneas hayan sido modificadas.
* Si se hace un ">>git stash" con un archivo modificado y luego se modifica el archivo, al momento de hacer ">>git stash pop" este archivo dará lugar a un conflicto.
* Si un desarrollador está modificando un archivo en una rama y esa misma rama tiene un commit que no ha sido descargada por el desarrollador al momento de hacer "push" habrá un conflicto en caso de que ese archivo haya sido modificado en los commits no descargados. 
### Resolver conflictos
1. Si el conflicto sale de manera espontánea saltar al paso #7
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
Se ve claramente la separación entre los dos cambios. </br>
8. Para solucionar el conflicto solo hay que deshacerse de los separadores, obviamente estoy hay que hacerlo de manera que el código funcione correctamente, **esta es la parte difícil de la resolución de conflictos y hay que hacerla con mucho tacto**.</br>
9. Luego de solucionar el conflicto hacer el **flujo normal** ósea git add, commit, push.</br>
10. Por último hacer de nuevo el pull request, el merge o lo que se estaba realizando.

## TODO: 
* ~~Tema de conflictos~~
* ~~Como instalar git~~
* ~~Solución de erratas~~
* ~~Video de YouTube~~
* Traduccion al ingles

<hr>
<div align="center">
<h3 align="center">Let's connect 😋</h3>
</div>
<p align="center">
<a href="https://www.linkedin.com/in/hector-pulido-17547369/" target="blank">
<img align="center" width="30px" alt="Hector's LinkedIn" src="https://www.vectorlogo.zone/logos/linkedin/linkedin-icon.svg"/></a> &nbsp; &nbsp;
<a href="https://twitter.com/Hector_Pulido_" target="blank">
<img align="center" width="30px" alt="Hector's Twitter" src="https://www.vectorlogo.zone/logos/twitter/twitter-official.svg"/></a> &nbsp; &nbsp;
<a href="https://www.twitch.tv/hector_pulido_" target="blank">
<img align="center" width="30px" alt="Hector's Twitch" src="https://www.vectorlogo.zone/logos/twitch/twitch-icon.svg"/></a> &nbsp; &nbsp;
<a href="https://www.youtube.com/channel/UCS_iMeH0P0nsIDPvBaJckOw" target="blank">
<img align="center" width="30px" alt="Hector's Youtube" src="https://www.vectorlogo.zone/logos/youtube/youtube-icon.svg"/></a> &nbsp; &nbsp;
<a href="https://pequesoft.net/" target="blank">
<img align="center" width="30px" alt="Pequesoft website" src="https://github.com/HectorPulido/HectorPulido/blob/master/img/pequesoft-favicon.png?raw=true"/></a> &nbsp; &nbsp;

# **Git y GitHub**
[![Git](https://img.shields.io/badge/Git-fff1f2?style=for-the-badge&logo=git&logoColor=fb7185&labelColor=1c1917)]()
[![Github](https://img.shields.io/badge/Github-fafaf9?style=for-the-badge&logo=github&logoColor=fafaf9&labelColor=1c1917)]()
## **Git**

## **¿ Que es Git ?**

Es un sistema de control de versiones en forma local.

## **Instalacion de Git**

Ir a la pagina de 
[git](https://git-scm.com/ "git")
y descargar la ultima version segun el sistema operativo que tengas.

> Para verificar que instalaste de manera correcta "Git" ,ve a tu terminal e ingresa : `git --version` o `git -v` 

> ### **Algunos comandos de la terminal que vale la pena saber**
>
> * `ls` : Se muestra un listado de todos los directorios que se tienen dentro de una carpeta.
> * `cd './mi carpeta/` : Somos capaces de seleccionar una carpeta o directorio (mi carpeta) de un directorio principal.
> * `cd ..` : Seremos capaces de movernos a una carpeta o directorio anterior. 
> * `pwd` : Nos muestra la ruta exacta donde nos encontramos.
> * `mkdir "nueva carpeta"` : Podremos crear una carpeta o directorio (nueva carpeta).
> * `touch tuarchivo.txt` : Crea un nuevo archivo en el directorio seleccionado.
> * `type nul > tuarchivo.txt` : Crea un archivo nuevo en windows (esta es una alternativa a `touch tuarchivo.txt`).
> * `code .` : Abre VScode. 

## **Configuracion de Git**

Antes de utilizar los comandos basicos de git debemos configurar git ,en nuestra terminal, con los siguientes comandos.
* `git config` : Esto nos sirve para trabajar con la configuracion de git. 
* `git config --global` : Configuracion aplicada a nivel global. 
* `git config --global user.name "nombre de usuario"` : Configurando el nombre de usuario a nivel global. 
* `git config --global user.email` "micorreo@gmail.com" : Configurando el email del usuario a nivel global.

## **Comandos utiles**

* `git --help`, `git -h` : Comando que nos ayuda a ver algunos comando basicos (en este caso de git).
* `git init` : Permite que git funcione en una carpeta o directorio (raiz) seleccionado. Con este comando inicializamos un control de versiones en la carpeta seleccionada.

  > **Nota** : Despues de ingresar el comando ( `git init` ) la terminal nos mostrara el nombre del directorio ( `midirectorio` ) y la rama principal donde se esta trabajando ( `master` ). **Ejm** : `midirectorio master`
* `git branch -m main` : Permite que git cambie el nombre de la rama principal a  `main`
*  `git status` : Permite que git nos muestre el estado en el cual esta nuestra carpeta.
   > **Nota** : `git status` nos muestra en la terminal las siguientes sentencias :
   >
   >  ```bash 
   >  On branch main
   > 
   >  No commits yet
   >  
   >  Untracked files:
   >  (use "git add <file>..." to include in    what will be committed)
   >         README.md
   > 
   >   nothing added to commit but untracked   files present (use "git add" to track)
   >  ```
   > Estas sentencias nos indican que en la rama principal ( `main` ) aun no se ha hecho un `commit` y que tambien si queremos agregar un archivo para hacer nuestro primer `commit ` debemos utilzar el comando `git add`
*  `git add miarchivo` : Comando que nos permite agregar un archivo. 
   > **Ejm** : `git add README.md`
   >
   > **Nota** : Si luego de escribir `git add README.md` escribimos el comando `git status` , la terminal nos mostrara las siguientes sentencias
   >
   >  ```bash 
   >  On branch main
   > 
   >  No commits yet
   >  
   >  Changes to be committed:
   >  (use "git rm --cached <file>..." to unstage)
   >         new file:   README.md
   > 
   >   nothing added to commit but untracked   files present (use "git add" to track)
   >  ``` 

* `git add .` : Comando que nos permite agregar todos los archivos existentes de nuestro directorio.
  
  > **Nota** : Si queremos que git ignore un archivo o varios archivos debemos agregar el archivo `.gitignore` en nuestra carpeta principal. Dentro de esta carpeta debemos escribir el archivo o los archivos que deseamos ignorar ,de esta manera `**/.archivo_ignorado.txt` luego escribimos el comando `git add .gitignore` para agregarlo a la rama y que esta sepa que archivos ignorar.
* `git commit -m "Este es mi primer commit"` : Comando que nos permite realizar nuestro primer commit (la primera version/fotografia de nuestro archivo)
<!-- *aqui comienza los logs -->
* `git log` : Comando que nos permite verificar si el primer commit se hizo de manera correcta. Este comando nos muestra el **commit**, el **Autor** y la **fecha** cuando fue creado el commit ( nos muestra todo lo que hemos estado haciendo hasta ahora ).
* `git log --graph` : Comando que nos permite estilizar la informacion mostrada por `git log`.
* `git log --graph --pretty=oneline` : Comando que nos permite resumir en una sola linea la informacion mostrada por `git log` (nos muestra el hash ( identificador ) del **commit** y el nombre que le pusimos).
* `git log --graph --decorate --all --online ` : Comando que nos permite resumir en una sola linea la informacion mostrada por `git log` (nos muestra un hash ( identificador ) acortado del **commit** y el nombre que le pusimos).
* `git reflog` : Comando que nos muestra de manera mucho mas detallada todos los cambios que se han hecho hasta ahora.
* `git tag "mi_etiqueta"` : Comando que nos permite poner una etiqueta ( mi_etiqueta ) a todo lo que hemos avanzado hasta el ultimo commit.
* `git tag` : Comando que nos permite ver las etiquetas que hemos ido poniendo a nuestro proyecto.
<!-- *aqui comienza los checkout --> 
* `git checkout ./README.md` : Comando que nos permite volver a una version anterior de un archivo partiendo desde una version que no fue agregada con `git add`.
* `git reset` : Comando que nos permite ver que ficheros han sido modificados pero aun no han sido agregados a la rama ,para luego aplicar el comando `git checkout` y volver a su version anterior.
* `git checkout (ingrese el hash)` : Comando que nos permite ir al commit cuyo hash sea el ingresado.
* `git checkout HEAD` : Comando que despues de haber ingresado `git checkout (ingrese el hash)` coloca la cabeza de la rama en dicho hash.
* `git reset --hard (ingrese el hash)` : Comando que nos permite resetear todos los cambios que se han hecho hasta el hash ingresado.
* `git checkout (ingrese nombre del tag)` : Comando que nos permite ir al tag ingresado.
<!-- *aqui comienzan otros git -->
* `git config --global alias.ponunalias "log --graph"` : Comando que nos permite poner un alias a un comando de git ( en nuestro caso estamos poniendo el alias de **ponunalias** al comando `log --graph` ) .
* `git diff` : Comando que nos muestra los cambios en un archivo sin necesidad de haberlos guardado.
<!-- * git para equipos -->
* `git branch (ingrese el nombre de la nueva rama)` : Comando que nos permite crear una nueva rama. 
* `git switch (ingrese el nombre de una rama)` : Comando que nos permite cambiar de rama.
* `git merge (ingrese el nombre de una rama)` : Comando que nos permite mergear ( fusionar ) la rama ingresada con la rama en donde se esta trabajando.
* `git stash` : Comando que nos sirve para crear un commit local que no afecta a la rama principal.
* `git stash list` : Comando que nos sirve para mostrar los commit locales creados por `git stash`.
* `git stash pop` : Comando que nos sirve para recuperar el commit local creado por `git stash`.
* `git stash drop` : Comando que nos sirve para borrar un commit local creado por `git stash`.
* `git branch` : Comando que sirve para ver las ramas creadas.
* `git branch -d (ingrese el nombre de la rama)` : Comando que sirve para eliminar la rama ingresada.

## **GitHub**

## **¿ Que es GitHub ?**

Es un lugar ( red social para desarrolladores ) donde puedes guardar de forma segura , en un repositorio , el codigo en donde estas trabajando y a su vez interactuar con otros programadores que tambien estan trabajando en el mismo codigo o en otro.

## **Secciones**

* **Overview** : Seccion donde puedes ver tu perfil de usuario.
* **Repositories** : Seccion donde puedes ver los repositorios que haz creado.
* **Stars** : Seccion donde puedes ver tus repositorios favoritos.

## **¿Como se crea un repositorio?**

**1. Por Git**



**2. Por GitHub**

* Haz click en el boton **New**
* Escribe el **nombre** de tu nuevo repositorio.
* Escribe una **descripcion** de tu nuevo repositorio.
* Elige si quieres que tu nuevo repositorio sea **publico** o **privado**.
* Haz click en agregar un archivo **README.md** para crear un archivo que contenga la documentacion de tu proyecto.
* Añade bajo que **licencia** esta trabajara tu proyecto.
* Presiona el boton **Create repository**.
  

## **Autenticacion SSH**








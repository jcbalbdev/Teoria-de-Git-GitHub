# **Git y GitHub**

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
> * `code .` : Abre VScode. 

## **Configuracion de Git**

Antes de utilizar los comandos basicos de git debemos configurar git ,en nuestra terminal, con los siguientes comandos.
* `git config` : Esto nos sirve para trabajar con la configuracion de git. 
* `git config --global` : Configuracion aplicada a nivel global. 
* `git config --global user.name "nombre de usuario"` : Configurando el nombre de usuario a nivel global. 
* `git config --global user.email` "micorreo@gmail.com" : Configurando el email del usuario a nivel global.

## **Comandos utiles**
* `git init` : Permite que git funcione en una carpeta o directorio (raiz) seleccionado. Con este comando inicializamos un control de versiones en la carpeta seleccionada.

  >*Nota 1* : Despues de ingresar el comando ( `git init` ) Vscode nos mostrara la letra ( `U` ) al costado de los archivos. **Ejm** : `README.md    U`
  >
  >*Nota 2* : Despues de ingresar el comando ( `git init` ) la terminal nos mostrara el nombre del directorio ( `midirectorio` ) y la rama principal donde se esta trabajando ( `master` ). **Ejm** : `midirectorio master`
* `git brach -m main` : Permite que git cambie el nombre de la rama principal a  `main`
*  `git status` : Permite que git nos muestre el estado en el cual esta nuestra carpeta.
   > **Nota** : `git status` nos muestra en la terminal las siguientes sentencias :
   >
   >  ``` 
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
* `git --help`, `git -h` : Comando que nos ayuda a ver algunos comando basicos (en este caso de git). 





<!-- * algunos codigos de markdown -->
**tipos de texto**

este es un *texto en italica*

este es un **texto en negrita**

este es un ~~texto tachado~~

**listas desordenadas :**

* hola
* hi

**listas ordenadas :**

1. uno
2. dos

**enlaces**

**1. tipo 1**

[texto alternativo](www.google.com)

**2. tipo 2**

[texto alternativo](www.google.com "google")

> **esta es una cita**
> 
> *esta es una cita*

**lineas horizontales**

---
---

**bloques de codigos**

`console.log("hi code!")`

```python
print("hello!!")
```
```html
<h1>heading</h1>
```

**tablas**

| Nombre | Apellidos |
|--------|-----------|
| Jose   | Balbin    |

**imagenes**

![imagen](www.google.com "google")

<!--* GITHUB MARKDOWN -->
**GITHUB MARKDOWN**

emojis 

* simbolo de cuernos  ( :metal: )
* estrella ( :star: )
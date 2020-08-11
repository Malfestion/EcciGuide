# Guia de git y unix 
  
Alejandro Duarte Lobo  
B62386  
  
### Ingreso a Gitlab UCR
* Se puede entrar al gitlab de la UCR mediante el link: [git UCR](https://git.ucr.ac.cr)`
* Se puede ingresar con los credenciales de la cuenta institucional.
* Para crear un nuevo grupo de trabajo se da click en la pestaña `gropus->Your groups` y se da click en el boton `New Group`
* Para crear un repositorio, dentro del grupo se caclick en el boton `New project`
* Para agregar miembros al grupo se va a la pestaña `settings` a la izquierda de la pagina, luego a se va a `members` y se agregan usando el correo institucional.
  
### Guia de uso de Git
* En caso de ser **la primera vez** que se instala git se utilizan los siguiente comandos para definir la identidad del usuario:
```console
user@pc:~$ git config --global user.name "nombre"
user@pc:~$ git config --global user.email "correo"

```
* Para ***clonar** un repositorio de git a una carpeta local se utiliza el comando:
```console
user@pc:~$ git clone [url del proyecto]

```
De esta manera se crea una copia del repositorio en git en un repositorio local, en el cual podemos trabajar usando el **Working directory**.  
* Para **agregar** archivos modificados al **stage** se usa el comando:  
```console
user@pc:/Proyecto$ git add archivo

```
* Para **modificar** los archivos en el repositorio o "meterlos al castillo" se usa el comando:
 ```console
user@pc:/Proyecto$ git commit -m "descripcion clara de los cambios"

```
* Para **subir** los archivos modificados al repositorio original se usa el comando:
```console
user@pc:/Proyecto$ git push

```
  
* En caso de hacer un cambio en el Working directory y luego "arrepentirse", para **restaurar los cambios** se usa el comando:
```console
user@pc:/Proyecto$ git checkout archivo

```
Este comando agarra los archivos que estan en el repositorio local y le cae encima a los archivos en el Working directory.  
* En caso de hacer un add y arrepentirse, para **revertir el add**, es decir, lo que se subio al stage se usa el comando:
```console
user@pc:/Proyecto$ git reset

```
* Para **revisar el estado** del repositorio se usa el comando:
```console
user@pc:/Proyecto$ git status

```
  
### Comandos basicos y notas utiles de Unix:
* Se puede cambiar en la consola a bash en vez de shell que es mas "amigable" y se pueden usar comandos como ctrl k o ctrl u y demas.  
Se puede modificar /etc/shells para que bash sea el primero.  
  
   
* `pwd` se usa para ver en el directorio en el que estamos.  
  
  
* En los sistemas Unix todos los archivos estan organizados como un arbol que empieza desde el nodo Raiz, a diferencia de los discos de windows.
  
    
* `ls` -a permite ver archivos ocultos, -l permite ver la lista "larga" incluyendo peso y permisos, entre otros datos.
  
  
* Los permisos:
    * la primera letra indica si es un directorio o un archivo comun (d,-).
    * los primeros 3 permisos afectan al usuario que creo el archivo.
    * los segundos 3 permisos corresponden a los permisos de grupo.
    * los ultimos 3 permisos corresponden a los que no estan en ninguno de los anteriores.
    * r=read w=write x=execute -=no tiene permisos
    * Ejemplo: **drwxr-xr-x** 
  
  
* Se pueden cambiar los permisos de un archivo o directorio con el comando `chmod`


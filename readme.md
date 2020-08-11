# Guia Para acceder a servicios de la ECCI    
Alejandro duarte Lobo  
B62386  
  
## VPN e ingreso a la maquina virtual
1. Instalar **OpenVPN**.  
2. Descargar los archivos de configuracion del VPN de la ecci.  
3. Ingresar el siguiente comando en el directorio donde estan los archivos de configuracion:  
```console
user@pc:/VPNecci/ecci/$ sudo openvpn --config ecci.ovpn  
```
4. Ingresar el username y password que se usa normalmente para ingresar a los laboratorios.  
Una vez conectado, dejar esa terminal abierta, ya que si se cierra o se usa ctrl+c se cerraria el tunel a la red de la ECCI.  

5. Para **conectarse a la maquina virtual** usar el sigiente comando:  
```console
user@pc:~$ ssh ecciadm@ip  
```  
Siendo la ip, la que los profesores le asignen.  
  
6. se usa el password que los profesores proveen para ingresar a la maquina.  
A partir de este paso ya estaria conectado a su maquina virtual.  
   
## Configuracion de la maquina virtual  
* Para cambiar el password de la maquina virtual se utiliza el siguiente comando:  
```console
user@pc:~$ passwd  
```
Seguidamente se ingresa el password actual y luego el password al que se desea cambiar como lo indica la terminal.  

* Para crear un nuevo usuario se usa el siguiente comando:
```console
user@pc:~$ sudo adduser username
```
O tambien  
```console
user@pc:~$ sudo useradd -m username

```
La opcion -m es para crear una carpeta home/ del usuario.  
Seguidamente nos pedira el password de administrador.  
Despues se debe cambiar el password del usuario que acabamos de crear:  
```console
user@pc:~$ sudo passwd username
```
Cuando se usa `sudo` en este caso, no pregunta por el password anterior.   

## Ingreso al Cluster de Arenal
* Se puede visualizar el cluster en: arenal.ecci.ucr.ac.cr , sin embargo desde la pagina solo se pueden observar estadisticas.    
### Para ingresar al cluster:
* Ingresar el siguiente comando:  
```console
user@pc:~$ ssh user@arenal.ecci.ucr.ac.cr  
```
  
Donde el **user** es el numero de carnet con la primera letra en mayuscula y el **password** es asignado por el profesor.  
### Para trabajar dentro del cluster:
* Se puede cambiar del nodo principal a un nodo esclavo utlilizando ssh:
```console
user@pc:~$ ssh compute-0-0    
user@pc:~$ ssh compute-0-1   
```
etc    
  
  
* para volver al nodo principal se utiliza `ctrl+D`
* Cualquier archivo en en el directorio `/home` es accesible para cualquier nodo esclavo, son archivos compartidos.
* En el directorio `/share/appps/ejemplosECCI/` se encuentran varios ejemplos del uso de OpenMP y MPI, para ejecutarlos se copian a /hoome/ se compilan y se ejecutan.
  
  
### Gitlab UCR
* Se puede entrar al gitlab de la UCR mediante el link:git.ucr.ac.cr
* Se puede ingresar con la cuenta institucional.
* Para crear un nuevo grupo de trabajo se da click en la pesta;a gropus->Your groups y se da click en el boton `New Group`
* Para crear un repositorio, dentro del grupo se caclick en el boton `New project`
* Para agregar miembros al grupo se va a la pesta;a settings a la izquierda de la pagina, luego a members y se agregan usando el correo institucional.
  
  
  
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
  
  
* 

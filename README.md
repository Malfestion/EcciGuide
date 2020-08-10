# Guia Para acceder a servicios de la ECCI
## VPN e ingreso a la maquina virtual
1. Instalar OpenVPN.  
2. Descargar los archivos de configuracion del VPN de la ecci.  
3. Ingresar el siguiente comando en el directorio donde estan los archivos de configuracion:  
  >sudo openvpn --config ecci.ovpn  
4. Ingresar el username y password que se usa normalmente para ingresar a los laboratorios.  
Una vez conectado, dejar esa terminal abierta, ya que si se cierra o se usa ctrl+c se cerraria el tunel a la red de la ECCI.  

5. Para *conectarse a la maquina virtual* usar el sigiente comando:  
  >ssh ecciadm@ip  
Siendo la ip, la que los profesores le asignen.  
6. se usa el password que los profesores proveen para ingresar a la maquina.  
A partir de este paso ya estaria conectado a su maquina virtual.  
   
## Configuracion de la maquina virtual  
Para cambiar el password de la maquina virtual se utiliza el siguiente comando:  
>passwd  
Seguidamente se ingresa el password actual y luego al que se desea cambiar como lo indica la terminal.  

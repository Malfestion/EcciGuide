# Guia Para acceder al VP
## VPN e ingreso a la maquina virtual
1. Instalar OpenVPN
1. Descargar los archivos de configuracion del VPN de la ecci
1. Ingresar el siguiente comando en el directorio donde estan los archivos de configuracion:
  >sudo openvpn --config ecci.ovpn  
1. Ingresar el username y password que se usa normalmente para ingresar a los laboratorios  
Una vez conectado, dejar esa terminal abierta, ya que si se cierra o se usa ctrl+c se cerraria el tunel a la red de la ECCI  

1. Para *conectarse a la maquina virtual* usar el sigiente comando:
  >ssh ecciadm@ip
1. se usa el password que los profesores proveen para ingresar a la maquina.
A partir de este paso ya estaria conectado a su maquina virtual.
  

# **TIPS -- Configuracion Forward Proxy Interno SA**

## PROXY
http://lan.prx.aap.aysa.ad:3128 (all)
NO PROXY=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

## Environment
export HTTP_PROXY=http://lan.prx.aap.aysa.ad:3128 
export HTTPS_PROXY=http://lan.prx.aap.aysa.ad:3128 
export NO_PROXY=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

export http_proxy=http://lan.prx.aap.aysa.ad:3128 
export https_proxy=http://lan.prx.aap.aysa.ad:3128 
export no_proxy=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

## Ejemplo para Linux

- Editar el archivo .bashrc o .bash_profile en el **directorio de inicio del usuario** para el que se desea habilitar el proxy. Se puede usar el siguiente comando para editarlo:

__Editar el archivo:__
nano ~/.bashrc

__Agregar al final del Archivo__
export http_proxy=http://proxy_server_address:proxy_port/
export https_proxy=http://proxy_server_address:proxy_port/
export ftp_proxy=http://proxy_server_address:proxy_port/
export NO_PROXY=localhost,127.0.0.1,10.0.0.0/8,172.16.0.0/12,192.168.0.0/16,.aysa.ad

__Guarda los cambios y cierra el archivo.__
Recargar la configuración ejecutando el siguiente comando o cerrando y volviendo a abrir la terminal: __source ~/.bashrc__


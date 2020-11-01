# Guia de comandos básicos Gnu/Linux 


### pwd
El comando **pwd** nos retorna la ruta donde nos encontremos.
#### Ejemplo:
```bash
$ pwd
```
#### Salida:
```bash
/home/nucleognulinux/comandosBasicosGnuLinux
```

### **ls**
Nos muestra una lista con el contenido del directorio actual (o el que le pasemos como argumento) 
```bash
ls /home/usuario

# files length
ls node_modules | wc -l
 90
 
# files size
du -sh node_modules
 17M node_modules
```


### **ls –l**
Muestra una lista del contenido del directorio añadiendo información adicional de los ficheros o carpetas, como permisos, fecha y hora de creación o modificación, etc…


### **ls –a**
Muestra una lista de todos los ficheros del directorio, incluyendo los ficheros o carpetas ocultos.


### **cd**
nos lleva al directorio raíz.


### **cd..**
Subiremos un nivel en el árbol de directorios. Si por ejemplo nos encontramos en /home/usuario, con este comando nos iremos a /home.
```bash
/home/usuario $ ../		==>		/home $
```

### **wget**
Descargar archivos 
```bash
wget https://ruta.de/mi/archivo-a-descargar.extension
```

##Limpiando cache:
http://www.tecmint.com/clear-ram-memory-cache-buffer-and-swap-space-on-linux/

Primero cambiamos permiso en la terminal
```bash
sudo su
```
### **Clear cache**
######Clear PageCache only.
```bash
sync; echo 1 > /proc/sys/vm/drop_caches
```
######Clear dentries and inodes.
```bash
sync; echo 2 > /proc/sys/vm/drop_caches
```
######Clear PageCache, dentries and inodes.
```bash
sync; echo 3 > /proc/sys/vm/drop_caches 
```
### **Clear Swap Space**
```bash
swapoff -a && swapon -a
```
######Revisamos el espacio con
```bash
free -h
```
```bash
free -m
```

### ...

### curl
El comando **curl** es una herramienta de tranferencia de datos, soporta los protocolos: (DICT, FILE, FTP, FTPS, GOPHER, HTTP, HTTPS, IMAP, IMAPS, LDAP, LDAPS, MQTT, POP3, POP3S, RTMP, RTMPS, RTSP, SCP, SFTP, SMB, SMBS, SMTP, SMTPS, TELNET and TFTP). 

#### Ejemplo:
```bash
$ curl google.com
```
#### Salida:
```bash
<HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
<TITLE>301 Moved</TITLE></HEAD><BODY>
<H1>301 Moved</H1>
The document has moved
<A HREF="http://www.google.com/">here</A>.
</BODY></HTML>
```

### ...

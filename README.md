# **Direccionamiento** ![ubuntulogo](https://upload.wikimedia.org/wikipedia/commons/b/b5/Former_Ubuntu_logo.svg)


>Este es un repositorio para comprobar como funciona el direccionamiento en Linux (Ubuntu) :computer:



### *Generar un archivo llamado informe.txt con la siguiente información* :
  
  * Fecha(con formato %d-%m-%Y)
  * Espacio en disco(usaremos "df -h")
  * La memoria libre del sistema(usaremos "free -h")
  * Usuarios conectados(usaremos "who")


**NOTA:Usaremos un direccionamiento externo para evitar direccionar por cada línea de comando de nuestro script**


* Primero creamos nuestro archivo sctript llamado "info.sh"

    ```
    nano info.sh
    ```
    
* Vamos a usar el enunciado y sus comandos para elaborar nuestro script
```sh

#!/bin/bash
#para fecha
echo "Fecha: $(date +%d-%m-%Y)"
#espacio en disco
echo "El espacio en disco es:"
df -h
#memoria libre del sistema
echo "La memoria libre del sistema es: "
free -h
#usuarios conectados
echo "Los usuarios conectados son: "
who

```
* Una vez creado el script, comprobamos con el comando ls que se encuentra en nuestro directorio /home/1asir
  ![img1](img1.png)
* Ahora vamos a usar el direccionamiento externo para que nos mande la informacion de lo que hace el script a un archivo, el archivo informe.txt. Para ello usaremos el signo matemático > o >> segun queramos machacar el archivo o ir añadiendo información. Ejecutaremos el script con el comando sh + "nombreScript" y direccionamos, quedaría así:

  ```
  sh info.sh >> informe.txt
  ```
  ![img2](img2.png)

* Finalmente, para ver que contiene nuestra archivo y que nos ha ejecutado bien las lineas del script, utilizamos la sentencia cat + "nombre del archivo" para que nos lo muestre
  ```
  cat informe.txt
  ```
  ![img3](img3.png)

  <p xmlns:cc="http://creativecommons.org/ns#" >This work by <span property="cc:attributionName">Adrián Cabezuelo Expósito</span> is licensed under <a href="http://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1"></a></p> 

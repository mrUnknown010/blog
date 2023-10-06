---
title: Comandos Basicos Linux
---

---
## Instalación parrotOS 
_→ parrotsec.org: download security edition_

## Maquina virtual
_→ vmware.com_
   + file → new virtual machine → tipical recomended
   + maximun disk size:60gb
   + store virtual disk as a single file
   + customize hardware → memory:4gb →procesadores:2 →network adapter:bridged(replicate physical network connection  state)





---
**whoami** → usuario del sistema

**id**  → identificador de grupos del usuario 

**sudo su** → escalar privilegio, acceder como root 

**exit** → salir

**sudo** whoami → ejecutar comando como root

**cat archivo.txt** → leer contenido de un archivo

**which** cat → ver ruta absoluta de un comando

**|** → pipear o tratar la salida de un comando anterior

**grep** "hola" **-n** → filtrar y mostrar el numero de linea

**comand -v** id → ver ruta absoluta de un comando

**pwd** → muestra ruta en la que se esta posicionado

**ls** → lista contenido en la posicion actual

**ls -l** → lista contenido con mas detalles

**tree -L** 2 → lista contenido ramificado con **2** descenso

**cd** Desktop → ingresar a un directorio

**cd ..** → salir o retroceder un directorio

**echo $PATH** → muestra ruta de binarios de los comandos

**echo $HOME** → muestra ruta principal del usuario

_**/etc/passwd**_ → ruta de archivos con los usuarios,id grupo,id usuario,...

**echo $SHELL** → muestra tipo de shell (/etc/shells)

id **;** whoami → ejecutar bloque de comandos

id **&&** exit → ejecucion multiple, si el primero es exitoso se ejecuta el resto

**echo $?** → codigo de estado de comando anterior ejecutado

**2>/dev/null** → redirigir el stder o error

**&>/dev/null** → redirigir el stder y stdout

wireshark **&** → poner en segundo plano

**& disown** → poner en segundo plano y desligar del proceso padre

**exec** 3 **<>** file → descriptor de archivo creado con identificador **3**, **r** read,**w** write

**>&** 3 → agregar contenido al descriptor de archivo

**exec** 3 **>&-** → cerrar un descriptor de archivo

**exec** 5 **>&** 3 → crea copia o descriptor al descriptor, ambos trabajan sobre el mismo archivo

**touch** file.txt → crear archivo

**file** data → muestra tipo de archivo

**!$** → hace referencia al ultimo argumento

**>** → sustituir contenido de un archivo

**>>** → agregar contenido a un archivo

**nano** file → editar archivo

_**.rwx rwx rwx user group**_ → permisos (**.** archivo),(propietario),(grupos),(otros)

_**drwx rwx rwx user group**_ → permisos (**d** directorio),(propietario),(grupos),(otros)

**chmod o+w** file → cambiar permisos,**o**tros,**g**rupos,**u**suarios,**+** añadir,**-** quitar

**mkdir** directory → crear directorio

**rm -r** directory → eliminar recursivamente en caso de haber subcarpetas

**chgrp** group directory → cambiar grupo a un directorio 

**useradd** user **-s** /bin/bash **-d** /home/user → añadir usuario,**s** tipo shell, **d** directorio

**passwd** user → asignar contraseña al usuario

**chwon** user file → cambiar propietario a un recurso

**chown** user:group resource → cambiar propietario y grupo a un recurso

**su** user → cambiar o migrar de usuario

**groupadd** group → agregar o crear nuevo grupo

**usermod -a -G** group user → añadir al grupo a un usuario

|r - x|- w x|- - x|permisos |
|-----|-----|-----|---------|
|1 0 1|0 1 1|0 0 1|binario  |
|_2 1 0_|_2 1 0_|_2 1 0_|potencia |
|_2_    |_2_    |_2_    |base     |

|2<sup>0</sup> 2<sup>2</sup>|2<sup>0</sup> 2<sup>1</sup>|2<sup>0</sup>|
|-----|------|--|
|5    |3     |1 |

| r-x -wx --x| |
|------------|-|
| chmod 531  | |

**chmod +t** resource → permite que solo el creador pueda renombrar o eliminarlo

**lsattr** resource → ver los flags o permisos especiales

**chattr +i -V** resource → añade inmutabilidad

| **xargs** → tratar el output anterior en parelelo (linea a linea)

**find** file **-type f -perm 4000** → buscar files con permiso suid (-rw**s** | r-x | r-x)

**chmod 4**775 file _||_ **chmod u+s** file → dar permiso suid (añdir **4** or **+s**)

> Un binario suid se ejecuta temporalmente como root o de forma privilegiada.

```py
    #escalar privilegios con binario python suid
    import os
    os.setuid(0)
    os.system("zsh")
```

|    |                   |
|----|-------------------|
|**Suid**| aplica para users |
|**Sgid**| aplica para groups|

**find** file **-perm -2000** → buscar binarios sgid bajo el grupo root o propietario

**chmod 2**755 file _||_ **chmod g+s** file  → dar permiso gsid (-rw | x-**s** | r-x)

**getcap -r** / 2>/dev/null → 

**setcap** → 

**setcap -r** file → quitar capabiliti

_ _ _

**bin** →directorio estatico, se almacena los binarios necesarios que garantiza las funciones basicas a nivel de usuario.

**sbin** → almacena los binarios necesarios para tareas adminstrativas gestionadas por el superusuario, hace lo mismo que _/bin_ pero tareas del sistema y solo son gestionadas por root.

**boot** → directorio estatico, incluye todos los archivos y ejecutables que son necesarios en el arranque del sistema (aqui se encuentra el grud).

**dev** → incluye todos los dispositivos de almacenamiento en forma de archivo (conectados al sistema).

**etc** → almacena los archivos de configuracion, a nivel de componentes del sistema operativo como los programas y aplicaciones instaladas, debe contener solo archivos de configuracion y no binarios.

**home** → directorio del usuario estandar, incluye archivos temporales de aplicaciones ejecutadas en modo root.

**lib** → inlcuye bibliotecas esenciales que son necesarios para que se pueda ejecutar correctamente todo los binarios en _/bin_ y _/sbin_ asi como los modulos del kernel.

**lib64** → referida a la biblioteca para aplicaciones de 64bits.

**media** → es el punto de montaje de todos los volumenes logicos que se montan temporalmente (usb,etc).

**opt** → viene a ser como una extension del directorio _/usr_, pero aqui van los archivos de solo lectura que son parte de programas autocontenido.

**proc** → contiene informacion de los procesos y aplicaciones que se estan ejecutando en un momento determinado en el sistema, realmente no guarda como tal, porque se almacenan archivos virtuales por lo que su contenido es nulo, basicamente son listas de eventos del SO al momento de acceder.

**root** → directorio home del superusuario, raiz del sistema operativo.

**srv** → almacena archivos y directorios virtuales que proveen informacion del kernel relativas.

**sys** → al igual que _/proc_, contiene archivos virtuales que proveen informacion del kernel relativas a eventos.

**tmp** → almacena archivos temporales de todo tipo, ya sea de elementos del sistema o aplicaciones.

**usr** → almacena archivos de solo lectura y relativo a utilidades del usuario incluyendo todo el software insatalado a traves de los gestores de parquete de cada distribucion.

**var** → contiene archivos con informacion del OS, como logs email de los usuarios del sistema, base de datos, informacion almacenada en la cache, informacion ralativa a paquetes de aplicaciones almacenadas en _/opt_,etc. Se puede decir que actua como registro del sistema.

_ _ _


**hostname -i** → muestra las ip`s

**find** / **-name** dex\\* → buscar algo que inicie por _dex_ y que sigue algo

**find** / **-name** \\*dex\\\* → buscar que inicie por algo y que contiene _exd_ y que sigue algo

**ip a** → 

**awk 'NR\==2'** → mostrar la linea _2_

**awk '{print $1}' FS="/"** → filtrar el primer argumento tomando como delimitador la barra _/_

**cut -d** '/' **-f1** 1 → delimitar por la barra y filtrar el primer argumento

**bash** file.sh → ejecutar archivos bash sin permisos de ejecucion

**ping -c** 1 → verificar si esta funcionable un servidor

**awk "/name\\"Forget\\"/,/result/"** → grepar _" /desde/ , /hasta/ "_

**declare -a** array=(1,2,3) → declarar array y elementos

**declare -r** var → declarar una variable (**r** lectura, **a** array, **-i** entero)

**echo ${miarray[@]}** → muestra todo el contenido del array

**echo ${#miarray[@]}** → muestra cantidad de elementos

**echo ${miarray[-1]}** → muestra el ultimo del array

**unset miarray[0]** → quitar un elemento

**grep -oP '\\[.*?\\]'** → **oP** para crear expresion regular, **.\*?** indica toda la data entre los **[]**

**sed 's/^$/##/'** → _Sustituir lineas en blanco por algo_ 

---

**sshpass -p** 'pass' **ssh** user@host **-p** port → 

**ssh** user@host **-p** port → 

**cat ./**-, **cat /ruta/**-, **cat $(pwd)/**- → 

**cat "a file"**, **cat a\ file**, **cat a\***, **cat \*fi*** → 

**ls -a** → 

**find . -type f** → 

**find . -type f -print "%f\t%p\t%u\t%g\t%m\n"** → contenido de un archivo

**find . -type f -print "%f\t%p\t%u\t%g\t%m\n" | column -t** → 

**find .** → 

**find . -name** .file **| xargs cat** → 

_**rwx rwx rwx**_ → contenido de un archivo

**chmod o+w** file → contenido de un archivo

**chgrp** group resource → contenido de un archivo

**su** user → contenido de un archivo

**r-- -w- --x → 100 010 001 → 421** → contenido de un archivo

**chattr +i -v** resource → contenido de un archivo

**lsattr** → contenido de un archivo

**find . -name** name → contenido de un archivo

**which** comando → contenido de un archivo

**file** resource → contenido de un archivo

**time** find . -type f → contenido de un archivo

**find . -type f -readable !-executable -size 1000c** → 

**find . -type f | xargs cat | xargs** → contenido de un archivo

**tr -d "\n"** → contenido de un archivo

**tr -d "\t"** → contenido de un archivo

**head -n 1** → contenido de un archivo

**tail -n 1** → contenido de un archivo

**awk 'NR\==2'** → 

**sed 's/this/to this/'** → 

**sed 's/this/to this/g'** → 

**grep "^root"** → 

**grep -r "\w"** → buscar por palabras

**grep -vE "one|two"** → omitir varias palabras

| **sponge** file → sobreescribe el contenido del mismo archivo

| **tee** file → te crea nuevo archivo

**seq 1 10** → 

**sed '/^\s\*$/d'** → eliminar lineas vacias, **^** que inicie por

**grep** "word" **-n** → muestra numero de linea

**find** / **-user** user **-group** group **2>/dev/null** → 

firefox > /dev/null **2>&1** → convierte stder a stdim

firefox **&** → poner en segundo plano

**disown** → independizar proceso

**wc -l** → contar lineas

**wc -c** → contar caracteres

**awk '/word/'** file → modo grepeo

**awk '{print $2}'** → filtrar por argumento **2**

**cut -d ' ' -f 4** → delimitar **-d** y filtrar columna **-f**

**awk 'NF{print $NF}'** → muestra el ultimo argumento de linea

**rev** → revertir orden

**sort | uniq -u** → cadenas unicas, alternativo orden numerico→ **sort -u -n**

**unique** → cadenas unicas

**strings** file → imprime caracteres legibles

chmod +x **!$** → hace referencia al ultimo argumento

**base64** → encriptar en base64

**base64 -d** → desencriptar base64

**tr ' ' '\n'** → convierte **'esto'** a **'otro'**

**sed 's/ /\n/g'** → sustituye **/esto/** a **/otro/**

**tr 'word' 'other'** → sustituye caracter por caracter

**tr '[G-ZA-Fg-za-f]''[T-ZA-St-za-s]'** → rotaciones, root13

**xxd -r** file → revertir hexadecimal, **-ps** muestra solo el hexadecimal

**grep** "word" **-A** 2 → muestra **n** lineas **abajo**

**grep** "word" **-B** 2 → muestra **n** lineas **arriba**

**grep** word **-C** 2 → muestra **n** lineas **arriba y abajo**

**echo $?** → codigo de estado

**grep '^abc$'** → **^** inicia por, **$** que termine en, que sea igual

**7z l** file.zip → listar contenido de un comprimido

**7z x** file.zip → extraer comprimido

**less** → modo paginacion

**stat** → detalles (modificacion, creacion, etc)

```bash
#!/bin/bash
namedecompressed=$(7z l conten.gzip | grep 'name' -A 2 | tail -n 1 | awk 'NF{print $NF}')
7z x content.gzip > /dev/null 2>&1
while true;do
	7z l $namedecompressed > /dev/null 2>&1
	if [ "$(echo $?)" == "0" ];then
		decompressednext=$(7z l $namedecompressed | grep 'name' -A 2 | tail -n 1 | awk 'NF{print $NF}')
		7z x $namedecompressed > /dev/null 2>&1 && namedecompressed=$decompressednext
	else
		cat $namedecompressed; rm data* 2>/dev/null; exit 1
	fi
done
```

_export TERM=xterm_

**sudo systemctl start sshd** → 

_**nano /etc/ssh/sshd_config** , **PermitRootlogin yes**_ → 

**ssh-keygen** , **cp id_rsa.pub autorized_keys** , **id_rsa** → 

**ssh user@host** → 

**ssh-copy-id -i** id_rsa user@host → convierte el **id_rsa** en clave autorizada

**ssh -i** id_rsa user@host → conectarse usando el id_rsa

**pwdx** pid → indica la ruta origen de ejecucion de un proceso

**echo ''>/dev/tcp/127.0.0.1/** port → 

**bash -c "echo ' '>/dev/tcp/host/port" 2>/dev/null && echo "port open" || echo "port closed"** → 

**echo** "word" | **nc localhost** port → 

**openssl s_client -connect** host:port → realiza una conexion segura

**ncat --ssl** host port → realiza una conexion segura

**nmap --open -T5 -v -n -p**iport-lport host → 

**mktemp -d** → 

**chmod 600** id_rsa → permiso comun de claves id_rsa

**ssh -i** id_rsa user@host → 

**diff** old new → 

**grep -v** 'word' → omitir algo en el grepeo

**grep -v -E** 'word,word2' → omite varias palabras en el grepeo

**nestat -nat** → 

**ss -nltp** → puertos abiertos en hexadecimal

cat **/proc/net/tcp** → puertos abiertos en hexadecimal

_**python3** → **ox0016**=22_ → revertir hexadecimal port

echo **"obase=10;ibase=16;porthex" | bc** → revertir hexadecimal port

```bash
#!/bin/bash
old_proces=$(ps -eo command)
while true;do
new_proces=$(ps -eo command)
diff < (echo "$old_proces") < (echo "$new_proces") | grep -v -E "procmon|command"
old_proces=$new_proces
done
```

**ssh** user@host **-p** port **bash**→ 

-rw**s**r-x--- 1 user group → **s** suid, se ejecuta temporalmente como el proietario

**./binaryfile** → ejecutar binario

**./binary20** sh _OR_ **./binary20** bash **-p**→ 

- - -

**TCP** → garantiza el paquete, no se fragmenta en el camino, generalmente llega al destinatario

**UDP** → se fragmenta en el camino, se puede spoofear con facilidad, no garantiza la llegada correcta de paquetes

- - -

**nc -nlvp** port → ponerse en escucha en un puerto

**nc** host port → conectarse a un servidor

    Tareas cron se ejecutan a intervalos de tiempo a nivel de sistema, lo hace a cada minuto o segun a su configuracion

|minuto \*|hora \*|dia mes \*                       |mes \*            |dia semana *    |                             |
|--------|------|-----------------------------|-----|-----------------|----------------|
|*       |*     |*                                  |*                |*               |cualquier valor              |
|,       |,     |,                                  |,                |,               |separador de lista de valores|
|-       |-     |-                                  |-                |-               |valores de rango             |
|/       |/     |/                                  |/                |/               |valore de paso               |
|0-59    |0-23  |1-31                               |1-12 <br> JAN-DEC|0-6 <br> SUN-SAT|valores permitidos           |
|        |      |L ultimo dia del mes               |                 |L sabado        |                             |
|        |      |W dia laborable mas cercano        |                 |# dia n         |                             |
|        |      |LW ultimo dia laborable mas cercano|                 |? sin valor especifico|                       |
|        |      |? sin valor especifico             |                 |                |                             |

| **md5sum** → 

```bash
#!/bin/bash
for i in {0000..9999};do
	echo $i
done
```

cat file | **nc** host port | **grep -v -E** "Wrong|please"→ 

**echo $0** → 

cat **/etc/passwd | grep** "word" → 

_**press v**_ , _**ctrl+b**_ , _**shift+:**_ , _**:e /etc/bandit_pass/bandit26**_ 

**:set shell=/bin/bash** , **:shell** → 

    En un repositorio git clonado se puede ver los commit (cambios en codigo)

_ssh://bandit27-git@localhost:port/home/bandit27-git/repo_

**git log -p** _commit_ → revisar cambios en commit

**git branch** → List, create, or delete branches

**git branch -a** → ver ramas

**git checkout** branch → te permite desplazarte entre las ramas creadas por git branch

**git tag** → etiqueta que almacena datos adicionales, capturas en un momento del commit

**git show** tag →muestra detalles de un objeto, cambios que han existido, ver o leer tag,commit,etc

**git add -f** file → añdir archivo nuevo al proyecto dentro de un directorio

**git commit -m** "commit" → añadir commit , un nombre descriptivo

**git push -u** origin master → confirmar cambios realizados en una rama local

**$0** → tipo de shell

**who** → informacion de usuarios conectados

**echo $LOGNAME** → nombre de usuario

**echo $$** → numero de proceso de shell

**echo $#** → muestra cantidad de parametros introducidos

**echo "$@!"** → muestra los parametros introducidos

**export PATH=$PATH":~/"**## → modifica el archivo .bashrc, se pone en el PATH para ejecutar de cualquier lado

**echo "${var:position:amount}"** → sustituir o mostrar

**lsof -i:** port → muestra el proceso corriendo en ese puerto

**ps -eo command** → muestra comando ejecutados en un intervalo de tiempo

**(echo ' '>/dev/tcp/host/port) 2>/dev/null** → 

**kill %** → eliminar tareas o trabajos

**import** file.jpg → capturar pantalla

**kitty** command file.sh → ejecutar algo o abrirlo en una nueva terminal

```bash
    for i in $(seq 1 154);do
        timeout 1 bash -c "ping -c 1 192.168.1.$i"&
    done;wait
```

```bash
    function ctrl_c(){
        echo "saliendo...";exit 1;tput cnorm
    }
```

**trap ctrl_c INT** → indica el uso de ctrl_c

**tput civis** → oculta cursor

**tput cnorm** → muestra cursor

**whatch -n 1** ls -l → monitoriza cada segundo

**ghex** file → muestra magic number que indica tipo de archivo "list of signatures"


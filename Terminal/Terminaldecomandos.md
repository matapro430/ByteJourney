# Terminal de comandos

Autor/Fuente: varios
Estatus: Estudiando
Resumen: No
Modificado: 16 de noviembre de 2023 10:22
Creado: 16 de noviembre de 2023 6:08

- **Índice del Tema, Curso o Libro:**
- [Terminal de comandos](#terminal-de-comandos)
  - [**ANEXOS:**](#anexos)
  - [RESUMEN DE: Terminal de comandos](#resumen-de-terminal-de-comandos)
- [IDEAS](#ideas)
    - [Si usas Windows](#si-usas-windows)
    - [**flags comunes de ls**](#flags-comunes-de-ls)
    - [\***\*Usos más productivos: `cd`**](#usos-más-productivos-cd)
    - [\***\*Usos más avanzados: `touch`**](#usos-más-avanzados-touch)
    - [Como crear Alias](#como-crear-alias)
    - [**Copiar archivos: `cp`**](#copiar-archivos-cp)
    - [**Mover y Renombrar: `mv`**](#mover-y-renombrar-mv)
- [APUNTES](#apuntes)
    - [Definicion](#definicion)
    - [\***\*Comandos básicos\*\***](#comandos-básicos)
    - [Comando man](#comando-man)
    - [Comando ls](#comando-ls)
    - [Comando pwd](#comando-pwd)
    - [El comando **`cd`**](#el-comando-cd)
    - [El comando `touch`](#el-comando-touch)
    - [Limpiar la terminal](#limpiar-la-terminal)
    - [El comando **`cat`**](#el-comando-cat)
    - [El comando **`cp`**](#el-comando-cp)
    - [El comando **`mv`**](#el-comando-mv)
    - [El comando **`rm`**](#el-comando-rm)
- [RESUMEN](#resumen)


## **ANEXOS:**

---

- ## **🔗 Ligas, documentos y medios importantes:**

## RESUMEN DE: Terminal de comandos

---

# IDEAS

### Si usas Windows

**Cygwin** brinda a los usuarios de Windows la posibilidad de trabajar con herramientas y comandos típicos de sistemas tipo Unix, facilitando la transición para aquellos familiarizados con entornos Unix o Linux.

**Windows Subsystem for Linux (WSL):** Es una característica de Windows que te permite ejecutar un sistema operativo Linux directamente en tu máquina con Windows. Puedes instalar distribuciones completas de Linux y acceder a un entorno de línea de comandos de Linux desde la terminal de Windows. WSL facilita la ejecución de comandos y el uso de herramientas de la línea de comandos de Linux sin necesidad de una máquina virtual. Es una opción popular para quienes desean combinar las funcionalidades de Windows y Linux en un mismo entorno.

### **flags comunes de ls**

Muestra información detallada sobre archivos y directorios, incluyendo permisos, propietario, grupo, tamaño, fecha de modificación y nombre del archivo.

**-l (formato largo): `ls -l`**

**-a (mostrar archivos ocultos): `ls -a`**

### \***\*Usos más productivos: `cd`**

**Ir al directorio anterior:**

`cd -`

**Ir a un directorio padre:**

`cd ..`

**Directorios relativos:**

`cd ../directorio_relativo`

### \***\*Usos más avanzados: `touch`**

**Crear múltiples archivos a la vez: Puedes crear varios archivos al mismo tiempo separando sus nombres con espacios.**

```bash
touch archivo1.txt archivo2.txt archivo3.txt

```

**Actualizar la fecha y hora de acceso y modificación:**

```bash
touch -a -m nombre_del_archivo
```

Este comando actualiza la fecha y hora de acceso (**`-a`**) y modificación (**`-m`**) del archivo especificado. Esto puede ser útil si necesitas cambiar las marcas de tiempo de un archivo sin modificar su contenido.

### Como crear Alias

**Crear un alias para crear archivos:**

1. Abre o crea el archivo de configuración de Zsh, generalmente **`~/.zshrc`**, con tu editor de texto preferido. Por ejemplo:

   ```bash
   vim ~/.zshrc
   ```

2. Agrega el siguiente alias al final del archivo:

   ```
   alias createfile='touch'
   ```

   Esto creará un alias llamado **`createfile`** que ejecuta el comando **`touch`**.

3. Guarda el archivo y recarga la configuración de Zsh:

   ```bash
   source ~/.zshrc
   ```

   **Ejemplos de alias populares y útiles:**

4. **Alias para listar archivos y directorios de forma detallada:**

   ```
   alias l='ls -l --color=auto'
   ```

5. **Alias para cambiar al directorio padre:**

   ```
   alias ..='cd ..'
   ```

6. **Alias para listar procesos de forma detallada:**

   ```
   alias psa='ps aux'
   ```

7. **Alias para actualizar el sistema (en Fedora):**

   ```
   alias update='sudo dnf update'
   ```

8. **Alias para limpiar la pantalla:**

   ```
   alias cls='clear'
   ```

### **Copiar archivos: `cp`**

```bash
Copiar archivos:
cp archivo_origen archivo_destino

Copiar directorios y su contenido:
cp -r directorio_origen directorio_destino

Copiar varios archivos a un directorio:
cp archivo1 archivo2 archivo3 ... directorio_destino
```

### **Mover y Renombrar: `mv`**

**Mover y renombrar directorios:**

```bash
mv origen destino
```

**Mover varios archivos a un directorio:**

```bash
mv archivo1 archivo2 ... directorio_destino
```

# APUNTES

### Definicion

La terminal de comandos es una interfaz de texto que te permite comunicarte con tu computadora utilizando comandos escritos en lenguaje de texto. En lugar de hacer clic en iconos o menús gráficos, puedes escribir instrucciones específicas para realizar tareas como copiar archivos, mover carpetas o ejecutar programas. Es una forma eficiente de interactuar con tu computadora utilizando texto en lugar de acciones gráficas.

### \***\*Comandos básicos\*\***

```bash
# Lista de comandos y trucos en la terminal

pwd         # directorio actual - (print working directory)
whoami      # muestra el nombre del usuario actual
help        # ayuda
-h          # ayuda
--help      # ayuda
clear       # limpiar la terminal
ls          # lista los archivos del directorio actual
cd          # cambiarse de directorio
~           # representa el directorio home
/           # representa el directorio raíz
.           # representa el directorio actual
..          # representa el directorio padre, subir un nivel del actual
-           # representa regresar al directorio anterior
""          # directorios o archivos con espacios en blanco deben nombrarse entre comillas
touch       # crea un archivo
echo        # crea un archivo con contenido
cat         # visualiza el contenido de un archivo en la terminal
mkdir       # crea un nuevo directorio
rm          # elimina un archivo
rmdir       # elimina un directorio vacío
rm -r       # elimina un directorio y su contenido
rm -rf      # forza a elimina un directorio y su contenido
mv          # mueve archivos o directorios
cp          # copia archivos
cp -r       # copia directorios y su contenido
find        # busca archivos o directorios
ps          # lista procesos activos
kill        # elimina un proceso activo
vim         # abre el editor VIM
nano        # abre el editor Nano
code        # abre el editor VS Code
alias       # crear un atajo personalizado a un comando largo
unalias     # elimina alias
```

### Comando man

El comando **`man`** es una herramienta valiosa para aprender sobre nuevos comandos y para obtener información detallada sobre cómo utilizarlos en sistemas basados en Unix y Linux.

```bash
man nombre_del_comando
man ls
```

La página del manual proporciona información sobre la sintaxis del comando, opciones disponibles, descripción de su funcionamiento y, en algunos casos, ejemplos de uso. Puedes navegar por las páginas del manual usando las teclas de flecha, y para salir, generalmente se presiona la tecla **"q"** para cerrar el visor del manual.

### Comando ls

El comando **`ls`** es uno de los comandos básicos en sistemas operativos Unix y Linux, y se utiliza para listar archivos y directorios en el directorio actual.

### Comando pwd

El comando **`pwd`** (print working directory) se utiliza para imprimir o mostrar el directorio de trabajo actual en la terminal.

### El comando **`cd`**

Este comando te lleva al directorio especificado. Puedes especificar la ruta completa o relativa al directorio al que deseas moverte

### El comando `touch`

se utiliza para **crear archivos** vacíos o actualizar la fecha y hora de acceso y modificación de archivos existentes.

**Comando básico para crear un archivo vacío:**

```bash
touch nombre_del_archivo

touch archivo.txt
```

### Limpiar la terminal

se refiere a eliminar el contenido actual de la pantalla para obtener una interfaz limpia y sin desorden.

Este comando simplemente borra la pantalla y te proporciona una terminal limpia.

```bash
clear
```

Presionar **`Ctrl + L`** (es decir, mantener presionada la tecla Control y presionar la tecla "L") generalmente realiza una acción similar a **`clear`** en muchas terminales.

`Ctrl + L`

### El comando **`cat`**

para concatenar y mostrar el contenido de archivos. Aunque su función principal es concatenar, también se utiliza comúnmente para mostrar el contenido de un archivo completo en la terminal.

**Mostrar el contenido de un archivo:**

```bash
cat nombre_del_archivo
```

Este comando muestra el contenido completo del archivo especificado en la terminal.

**Concatenar varios archivos y mostrar el resultado:**

```bash
cat archivo1 archivo2 archivo3
```

Al proporcionar varios nombres de archivo como argumentos, **`cat`** concatena sus contenidos y los muestra en la terminal. Puedes redirigir la salida a un nuevo archivo si deseas crear un archivo concatenado:

```bash
cat archivo1 archivo2 archivo3 > archivo_concatenado

```

**Concatenar y mostrar el contenido de un archivo junto con el número de línea:**

```bash
bashCopy code
cat -n nombre_del_archivo

```

El flag **`-n`** agrega números de línea al contenido del archivo.

**Mostrar el contenido de varios archivos con encabezados:**

```bash
cat -n archivo1.txt archivo2.txt | tee archivo_concatenado.txt
```

El comando anterior utiliza **`tee`** para mostrar la salida en la terminal y guardarla en un nuevo archivo (**`archivo_concatenado.txt`**).

**Concatenar el contenido de un archivo y mostrar las líneas numeradas:**

```bash
cat -n nombre_del_archivo | less
```

El comando anterior utiliza **`less`** para mostrar el contenido de un archivo página por página, lo que puede ser útil para archivos largos.

### El comando **`cp`**

para **copiar archivos** o directorios de un lugar a otro

**Copiar un archivo a otro lugar:**

```bash
cp archivo_origen ruta_destino
cp documento.txt /ruta/del/directorio
```

\***\*Copiar un directorio y su contenido:\*\***

```bash
cp -r directorio_origen ruta_destino
cp -r carpeta1 /ruta/del/destino
```

### El comando **`mv`**

para mover o renombrar archivos y directorios.

**Mover un archivo a otro lugar:**

```bash
mv archivo_origen ruta_destino
```

Esto mueve el archivo desde la ubicación especificada como **`archivo_origen`** a la ubicación especificada como **`ruta_destino`**.

Ejemplo:

```bash
mv documento.txt /ruta/del/directorio
```

**Mover y renombrar un archivo:**

```bash
mv archivo_origen archivo_destino
```

Esto renombra el archivo desde **`archivo_origen`** a **`archivo_destino`**.

Ejemplo:

```bash
mv archivo_antiguo.txt archivo_nuevo.txt
```

**Mover un directorio y su contenido:**

```bash
mv directorio_origen ruta_destino
```

Esto mueve el directorio y su contenido desde **`directorio_origen`** a **`ruta_destino`**.

Ejemplo:

```bash
mv carpeta1 /ruta/del/destino
```

**Mover y renombrar un directorio:**

```bash
mv directorio_origen directorio_destino
```

Esto renombra el directorio desde **`directorio_origen`** a **`directorio_destino`**.

Ejemplo:

```bash
mv viejo_directorio nuevo_directorio
```

**Mover varios archivos a un directorio:**

```bash
mv archivo1 archivo2 archivo3 ... directorio_destino
```

Esto mueve varios archivos a un directorio especificado.

Ejemplo:

```bash
mv imagen1.jpg imagen2.jpg /ruta/de/imagenes
```

**Confirmar antes de sobrescribir archivos:**

```bash
mv -i archivo_origen archivo_destino
```

El flag **`-i`** solicitará confirmación antes de sobrescribir un archivo existente en el destino.

Ejemplo:

```bash
mv -i documento.txt /ruta/de/backup
```

### El comando **`rm`**

se utiliza para eliminar (borrar) archivos y directorios. Ten en cuenta que este comando es muy poderoso y permanente, ya que elimina los archivos sin enviarlos a la papelera de reciclaje.

**Eliminar un archivo:**

```bash
bashCopy code
rm nombre_del_archivo

```

Esto elimina el archivo especificado.

Ejemplo:

```bash
bashCopy code
rm documento.txt

```

**Eliminar varios archivos:**

```bash
bashCopy code
rm archivo1 archivo2 archivo3 ...

```

Esto elimina varios archivos especificados en una sola línea de comando.

Ejemplo:

```bash
bashCopy code
rm imagen1.jpg imagen2.jpg

```

**Eliminar un directorio y su contenido de forma recursiva:**

```bash
bashCopy code
rm -r nombre_del_directorio

```

El flag **`-r`** (o **`-R`**) indica que se debe eliminar de forma recursiva, incluyendo el contenido del directorio.

Ejemplo:

```bash
bashCopy code
rm -r carpeta1

```

**Eliminar un directorio y su contenido sin confirmación:**

```bash
bashCopy code
rm -rf nombre_del_directorio

```

El flag **`-rf`** significa "force" (forzar) y "recursive" (recursivo), eliminando el directorio y su contenido sin solicitar confirmación.

Ejemplo:

```bash
bashCopy code
rm -rf carpeta_a_eliminar

```

**Solicitar confirmación antes de eliminar cada archivo:**

```bash
bashCopy code
rm -i nombre_del_archivo

```

El flag **`-i`** solicitará confirmación antes de eliminar cada archivo.

Ejemplo:

```bash
bashCopy code
rm -i archivo.txt

```

---

# RESUMEN

¡Felicidades por embarcarte en este viaje de descubrimiento en el mundo de la terminal! Hemos explorado desde los fundamentos hasta trucos avanzados, y ahora estás equipado con conocimientos para navegar y dominar la terminal como un verdadero experto.

Puntos Destacados:

- **Navegación en la Terminal:**

Descubre las alternativas para usuarios de Windows como Cygwin y WSL.
Aprende comandos esenciales como ls y cd.

- **Comandos y Trucos Esenciales:**

Utiliza touch para crear archivos y gestionar fechas de modificación.
Personaliza tu experiencia con alias en Zsh.

- **Gestión Avanzada de Archivos:**

Copia (cp) y mueve (mv) archivos y directorios con eficacia.

- **Comandos Útiles para Todos:**

Visualiza y concatena contenido de archivos con cat.
Ejecuta con precaución al utilizar rm para eliminar archivos y directorios.

- **Enfoque Especial en Windows:**

Descubre las ventajas de Cygwin y WSL para usuarios de Windows.
Estos apuntes no solo te ofrecen conocimientos prácticos, sino que también te invitan a personalizar tu experiencia en la terminal. ¡Ahora estás listo para aprovechar al máximo este recurso poderoso y versátil!

¡Que tu travesía en el mundo de la terminal sea emocionante y llena de descubrimientos!


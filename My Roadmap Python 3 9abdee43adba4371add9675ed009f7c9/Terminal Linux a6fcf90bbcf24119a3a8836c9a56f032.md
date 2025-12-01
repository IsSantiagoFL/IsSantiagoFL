# Terminal Linux

*Autor: Santiago I. Flores*

**Capítulo 1: Introducción a la Terminal y Línea de Comando en Linux**

La terminal y la línea de comando son herramientas esenciales para interactuar con un sistema operativo basado en Unix, como Linux.

### Terminal (Emulador de Terminal):

La “terminal” es una ventana especial que proporciona acceso directo a la *línea de comando* de un sistema operativo. Al abrir la terminal, te enfrentas a una pantalla de texto en la que puedes interactuar con la computadora mediante comandos. La terminal aloja a lo que se conoce como "shell", que es el intérprete de comandos que procesa tus instrucciones y las comunica al sistema operativo para que se realicen acciones.

### Línea de Comando (Shell):

La línea de comando, o shell, es un programa que acepta comandos escritos por el usuario y los traduce en acciones que el sistema operativo puede entender y ejecutar. A través de la línea de comando, puedes realizar una variedad de tareas, desde la gestión de archivos y directorios hasta la configuración del sistema y la ejecución de programas. Es la puerta de acceso a la funcionalidad profunda y poderosa de tu sistema operativo.

## Comando:

Un comando es un programa o una instrucción que puedes ejecutar en la línea de comando. Los comandos pueden recibir parámetros y opciones para modificar su comportamiento. Desde la gestión de archivos hasta la configuración del sistema, los comandos son las herramientas con las que puedes interactuar directamente a través de la terminal.

## Tipos de Shells:

| Shell |  |
| --- | --- |
| PowerShell | es el shell predeterminado en sistemas Windows. Está diseñado para la automatización avanzada y la administración del sistema. |
| Bourne Shell | Una de los primeros shells desarrollados, sienta las bases para muchos otros. Aunque es bastante básico, su simplicidad puede ser útil para principiantes. |
| C Shell | se destaca por su sintaxis similar al lenguaje C. Aunque no es tan popular en la actualidad, algunos usuarios prefieren su estilo de interacción. |
| Korn Shell | busca combinar las mejores características del Bourne Shell y el C Shell. Ofrece mejoras en la eficiencia de scripting y en la interacción del usuario. |
| Bash Shell | ampliamente utilizado en sistemas Linux. Destaca por su versatilidad y amplio conjunto de características. Su interfaz familiar y su amplia documentación lo convierten en una excelente opción para usuarios de todos los niveles.

El Bash (Bourne Again Shell) es común en la mayoría de las distribuciones de Linux y generalmente es la shell predeterminada en muchas de ellas, incluyendo Ubuntu, Debian, Fedora y más. También está disponible en otros sistemas operativos y se puede instalar en macOS y Windows.

incorpora características útiles del shell Korn (ksh) y el shell C (csh). |
| Z Shell (Zsh) | es una evolución del Bash Shell que ofrece características adicionales y una experiencia de usuario mejorada. Sus capacidades de autocompletado y personalización son especialmente apreciadas.

Aunque es comúnmente asociado con macOS debido a su potencia y características, el Zsh no es la shell predeterminada en macOS, que utiliza Bash de forma predeterminada. Sin embargo, los usuarios avanzados a menudo optan por instalar Zsh por sus características adicionales. También está disponible para Linux y otros sistemas Unix. |
| Fish Shell | se centra en la facilidad de uso y la autocomprensión. Sus sugerencias contextuales y su diseño intuitivo son ideales para nuevos usuarios. 

Su diseño intuitivo y sugerencias contextuales son beneficiosas para los profesionales que desean un entorno de trabajo más amigable. Fish facilita la exploración de datos y la realización de análisis complejos al reducir la carga cognitiva. |
| Ash Shell | Esta es otra shell minimalista que a menudo se utiliza en sistemas Unix y Linux en entornos con recursos limitados, como sistemas empotrados o dispositivos de bajo consumo. |
| Dash Shell | Esta es una shell minimalista y rápida que a menudo se utiliza en sistemas Unix y Linux para tareas internas y de arranque. En algunos sistemas Linux, como Ubuntu, Dash se utiliza como el intérprete predeterminado para scripts de inicio. |
| Oil Shell | Se trata de un proyecto en desarrollo que tiene como objetivo crear una shell compatible con Bash pero con mejoras de diseño y rendimiento. Su objetivo es ser compatible con scripts de Bash existentes mientras ofrece una sintaxis más predecible y una mayor velocidad. |
| Elvish | Es una shell moderna y extensible que se centra en la interactividad y la programabilidad. Ofrece características únicas como el autocompletado por tipo de valor y la manipulación directa de datos estructurados. |
| Nu Shell | Se trata de una shell orientada a objetos y basada en texto que busca simplificar la manipulación y visualización de datos. Ofrece una sintaxis más legible y accesible para el manejo de archivos y comandos. |
| Xonsh | Una shell que combina características de Python con la interactividad de las shells tradicionales. Permite escribir comandos en Python mientras mantiene la capacidad de ejecutar comandos del sistema. |

**Capítulo 2: Sistema de Archivos de un Sistema Linux**

En este capítulo, exploraremos el sistema de archivos de un sistema Linux y cómo se estructura, con el fin de proporcionarte una comprensión sólida del entorno en el que operarás a través de la terminal.

# **Estructura del Sistema de Archivos en Linux**

El sistema de archivos de Linux se organiza jerárquicamente en forma de un árbol. Cada "directorio" (no se utiliza el término "carpeta" en Linux) contiene archivos y subdirectorios. 

**A continuación se presentan algunos de los directorios más importantes:**

```markdown
- **/** *(Raíz del Sistema de Archivos): Contiene todos los demás directorios*
	- **/var** *Contiene datos variables, como registros, cachés y archivos temporales.*
	- **/usr** *Aquí se almacenan los programas y archivos del sistema.*
		- **/lib** *Bibliotecas compartidas utilizadas por programas en /usr.*
	- **/dev** *Contiene archivos que representan dispositivos físicos y virtuales.*
	- **/etc** *Archivos de configuración del sistema.*
	- **/home** *Los directorios de los usuarios, se almacenan archivos personales.*
		- **/username** *El directorio personal de cada usuario.*
```

Ejemplo: A continuación muestro el árbol de sistemas de archivos de mi sistema operativo

```markdown
(base) santiago@santiago-MS-7640:/$ tree -L 1
.
├── bin
├── boot
├── cdrom
├── dev
├── etc
├── **home**
		└── **santiago**
		    ├── **Descargas**
		    ├── **Documentos**
		    ├── **Escritorio**
		    ├── GitHub
		    ├── **Imágenes**
		    ├── **Música**
		    ├── octave
		    ├── **Plantillas**
		    ├── Programas
		    ├── **Público**
		    ├── R
		    ├── snap
		    ├── **Vídeos**
		    └── VirtualBox VMs
├── lib
├── lib32
├── lib64
├── libx32
├── lost+found
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── snap
├── srv
├── swapfile
├── sys
├── tmp
├── usr
└── var
```

Se recomienda ver el siguiente video para complementar la información anteriormente mostrada.

[https://youtu.be/TEZ26QWo9Yk](https://youtu.be/TEZ26QWo9Yk)

---

# **Estructura por Defecto del Shell Bash**

Cuando abres la terminal, verás una línea que muestra información sobre tu sesión actual. La estructura típica de la línea de comandos de Bash es la siguiente:

```bash
username@hostname:current_directory$
```

Cuando se está trabajando en un entorno virtual, la anatomía es la siguiente:

```bash
(evnname) username@hostname:current_directory$
```

Donde: 

- **(evnname)**: Nombre del entorno virtual que se está ejecutando
- **username**: Tu nombre de usuario.
- **hostname**: El nombre de la máquina.
- **current_directory**: El directorio actual en el que te encuentras.
- **$**: *prompt* (indicador de comandos), indica que el sistema está listo para recibir un comando por parte del usuario. A continuación del *prompt* es donde puedes escribir tus comandos y consultas.

---

# **Comandos Básicos de Bash**

![Untitled](Terminal%20Linux%20a6fcf90bbcf24119a3a8836c9a56f032/Untitled.png)

A continuación, te presentamos algunos de los comandos básicos más útiles en Bash que te permitirán navegar y trabajar eficazmente en el sistema de archivos:

- **ls**: Lista los archivos y directorios en la ubicación actual.
- **cd**: Cambia de directorio.
- **clear**: Limpia la terminal.
- **ctrl + L**: También limpia la terminal.
- **ls -l**: Muestra una lista detallada de archivos y directorios.
- **ls -lh**: Muestra una lista detallada con tamaños legibles por humanos.
- **pwd**: Muestra la ruta completa del directorio actual.
- **.**: Se refiere al directorio actual.
- **..**: Se refiere al directorio padre.
- **file**: Describe el tipo de archivo.
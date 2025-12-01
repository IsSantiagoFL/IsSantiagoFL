# Conda y Anaconda

****************************Hoja de trucos****************************

[Cheat sheet — conda 23.7.3.dev29 documentation](https://docs.conda.io/projects/conda/en/latest/user-guide/cheatsheet.html)

---

---

# 1. Descargar Anaconda

Primero tendremos que instalar la herramienta ********wget******** en Linux para descargar Anaconda desde Internet.

**`wget`** es una herramienta simple y poderosa que permite descargar archivos desde la web. Si no lo tienes instalado, puedes hacerlo con:

```bash
sudo apt-get install wget
```

```bash
wget -O anaconda.sh [URL_de_descarga]
```

Por ejemplo:

```bash
wget -O anaconda.sh https://repo.anaconda.com/archive/Anaconda3-2023.07-2-Linux-x86_64.sh
```

Como alternativa a ********`wget`******** también se puede usar **`curl`** o **`aria2`** en sistemas Linux.

# 2. Instalar Anaconda

```bash
bash anaconda.sh
```

Al terminar la instalación de Anaconda, reiniciar la terminal para que los cambios surjan efecto. 

# 3. Uso de Conda con Anaconda

> **Introducción a los Entornos Virtuales:** Un entorno virtual es un espacio aislado donde puedes instalar paquetes sin afectar otros proyectos o el sistema en general. Esto es especialmente útil para gestionar dependencias y asegurarte de que tu proyecto funcione consistentemente en diferentes máquinas.
> 

### **1. Introducción a Conda y Anaconda**

- **Conda**: Es un sistema de gestión de paquetes y un gestor de entornos virtuales. Permite instalar múltiples versiones de paquetes y software sin que estos entren en conflicto entre sí.
- **Anaconda**: Es una distribución de Python y R que incluye una gran cantidad de paquetes científicos y de análisis de datos. Básicamente, es un conjunto preempaquetado que incluye **`conda`**, Python, y muchos paquetes útiles para la ciencia de datos.

<aside>
⚠️ **Diferencia entre `pipenv` y `conda`**

- **pipenv**: Es una herramienta de gestión de dependencias y entornos virtuales para Python. Se basa en **`pip`** y **`virtualenv`**. Es específico para proyectos Python y se utiliza principalmente para gestionar las dependencias de un proyecto y asegurar que todas las dependencias estén en la versión correcta.
- **conda**: Es un gestor de paquetes y entornos virtuales que no se limita solo a Python. Puede manejar paquetes de múltiples lenguajes y es especialmente útil cuando se trabaja con paquetes que tienen dependencias complicadas, como bibliotecas científicas que requieren enlaces a lenguajes como C o Fortran.

**¿Cuál usar?** Depende de tus necesidades:

- Si estás trabajando en un proyecto Python puro y quieres una herramienta que gestione dependencias y entornos virtuales, **`pipenv`** es una excelente opción.
- Si estás trabajando con proyectos que involucran múltiples lenguajes o con paquetes científicos que tienen dependencias complicadas, **`conda`** es probablemente la mejor opción.
</aside>

### **2. Comandos Básicos de Conda**

- **Ver información del ambiente Conda**: Este comando te mostrará detalles sobre tu instalación de conda, la versión, los entornos que tienes creados, etc. Sirve para verificar si conda esta instalado y ver la versión instalada.
    
    ```bash
    conda info
    ```
    

### **3. Jupyter Notebook y Jupyter Lab**

- **Jupyter Notebook**: Es una aplicación web que permite crear y compartir documentos que contienen código en vivo, ecuaciones, visualizaciones y texto narrativo. Es ampliamente utilizado en análisis de datos, ciencia de datos, investigación científica, entre otros.
    
    Para abrir un Jupyter Notebook, simplemente escribe:
    
    ```bash
    jupyter-notebook
    ```
    
- **Jupyter Lab**: Es una interfaz de usuario web de próxima generación para el Proyecto Jupyter. Ofrece todas las funcionalidades de Jupyter Notebook (notebook, terminal, editor de texto, explorador de archivos, etc.) pero con una interfaz más moderna y extensible. Puedes pensar en Jupyter Lab como una evolución o un "IDE" para Jupyter.
    
    Para abrir Jupyter Lab, escribe:
    
    ```bash
    jupyter lab
    ```
    

<aside>
🐍 **Diferencia entre Jupyter Notebook y Jupyter Lab**

- **Interfaz**: Jupyter Lab tiene una interfaz más moderna y es más extensible que Jupyter Notebook.
- **Funcionalidades**: Jupyter Lab es como un entorno de desarrollo integrado (IDE) para Jupyter. Puedes tener múltiples notebooks abiertos en pestañas, editar archivos de texto, visualizar imágenes, entre otras cosas, todo en una misma ventana.
- **Extensibilidad**: Jupyter Lab es más fácil de extender con complementos y tiene un sistema de extensiones más robusto.
- **Adopción**: Aunque Jupyter Notebook todavía es ampliamente utilizado, Jupyter Lab está ganando terreno rápidamente debido a sus características avanzadas.
</aside>

### **4. Jupyter y VSCode**

VSCode (Visual Studio Code) es un editor de código fuente desarrollado por Microsoft. Con las extensiones adecuadas, puedes usar Jupyter directamente dentro de VSCode.

- Para trabajar con Jupyter en VSCode, necesitas tener instalado **`jupyter`**. No es estrictamente necesario tener todo Anaconda, pero Anaconda facilita la gestión de paquetes y entornos.

<aside>
💡 Si solo tienes Python y VSCode (y no Anaconda), puedes instalar Jupyter usando **`pip`**:

```bash
pip install jupyter
```

</aside>

- Una vez instalado, y con la extensión de Jupyter en VSCode, puedes crear y abrir notebooks directamente desde el editor.

<aside>
➡️ **Guía para Abrir Notebooks en VSCode con Ambientes de Conda**

Si ya tiene instalado Anaconda y creado un ambiente virtual con conda, también se puede VSCode para abrir notebooks Jupyter.

1. **Pasos para abrir Notebooks en VSCode**:
    
    a. **Iniciar Visual Studio Code**:
    
    - Ejecuta el comando **`code .`** en tu terminal para abrir VSCode.
    
    b. **Abrir o Crear Notebook**:
    
    - Abre la notebook que creaste anteriormente o crea una nueva con el nombre **`Untitled.ipynb`**.
    
    c. **Verificar Extensión de Python**:
    
    - Asegúrate de tener la extensión de Python instalada en VSCode.
    
    d. **Seleccionar Kernel**:
    
    - En la esquina superior derecha de tu notebook, encontrarás un botón que podría decir "Select Kernel", "Not Started" o mostrar un Kernel ya seleccionado. Haz clic en él.
    - Se mostrará una lista con todos los Kernels/ambientes instalados en tu computadora. Elige el ambiente que desees usar. Por ejemplo, puedes seleccionar el ambiente **`py39`** que se creó en clases anteriores.
    - Una vez seleccionado, el nombre del ambiente aparecerá en el botón en la esquina superior derecha.
2. **Solución de Problemas**:
    
    a. **Ambientes de Conda no mostrados**:
    
    - Asegúrate de tener instalada la extensión de Python en VSCode.
    - Si el problema persiste, recarga tu ventana de VSCode con **`Ctrl + R`** o **`Command + R`**.
    
    b. **Si el comando `code .` no funciona**:
    
    - Abre Visual Studio Code de manera regular.
    - Usa el atajo `ctrl + shift + p`.
    - Escribe “Shell Command” en la barra que aparece.
    - Selecciona “Shell Command: Install “code” command in shell PATH”.
    - Reinicia tu computadora.
    
    c. **Si tienes problemas ejecutando Jupyter Notebooks en nuevos ambientes virtuales**:
    
    - Es probable que no hayas instalado el paquete necesario. Ejecuta el siguiente comando:
        
        ```bash
        conda install ipykernel
        ```
        
</aside>

# 4. **Guía de Uso de Entornos Virtuales con Conda**

### 1**. El Entorno Base**

Al instalar Anaconda, automáticamente se crea un entorno llamado **`base`**. Este entorno se activará por defecto cada vez que abras una terminal, indicado por **`(base)`** al inicio de la línea de comandos.

### 2. **Listar Entornos Virtuales**

Para ver todos los entornos que tienes instalados:

```bash
conda env list
```

### 3**. Crear un Entorno Virtual**

> **Sintaxis de Comandos:**
Cuando ves un **`-`** antes de un comando, generalmente es una versión abreviada del comando. Por otro lado, **`--`** generalmente precede a una palabra completa o a una opción más descriptiva.
> 

Para crear un nuevo entorno virtual:

```bash
conda create --name py35 python=3.5 pandas
```

o lo que sería lo mismo:

```bash
conda create -n py35 python=3.5 pandas
```

Esto creará un entorno llamado **`py35`** con Python 3.5 y la última versión de pandas.

### Recom**endaciones para Nombrar Entornos Virtuales**

| Recomendación | Descripción | Bien ✅ | Mal ❌ |
| --- | --- | --- | --- |
| Descriptivo pero corto | El nombre debe dar una idea del propósito del entorno, pero también debe ser fácil de escribir y recordar. | ml-nlp-project | project1 o data-thing-that-does-stuff-with-text |
| Evitar Nombres Demasiado Largos | Un nombre de entorno virtual no debería ser una oración. Si sientes la necesidad de usar muchas palabras, probablemente puedas ser más específico sobre el propósito del entorno. | image_processing | project_for_processing_and_analyzing_images_from_cameras |
| Evitar espacios y caracteres especiales | Esto puede causar problemas en la terminal. | ecommerce_site | e-commerce site! |
| Usar Guiones Bajos o Guiones | Estos son fáciles de escribir y leer en la terminal. | data_cleaning o data-cleaning | datacleaning |
| Versiones | Si trabajas con diferentes versiones de Python o de un paquete específico, puedes incluir la versión en el nombre, como py35 o django3. | django3_project o py38_ml | project_with_new_python |
| Incluir Tecnologías o Versiones Relevantes | Si el entorno está diseñado para un proyecto que utiliza una versión específica de Python o una biblioteca, considera incluirlo en el nombre. | django3_project o py38_ml | project_with_new_python |
| Evitar Nombres de Paquetes Existentes | No uses nombres que puedan confundirse con paquetes o bibliotecas populares. Esto puede causar confusión. |  numpy_analysis | numpy |
| Evitar nombres genéricos o ambiguos | Nombres como "test" o "project" no son descriptivos y pueden ser confusos en el futuro. | finance_dashboard | new_project |
| Evitar Acronimos Ambiguos | A menos que el acrónimo sea ampliamente reconocido en tu equipo o industria, es mejor evitarlo o combinarlo con palabras descriptivas. | nlp_research | NLRP |
| Consistencia | Si estás trabajando en varios proyectos relacionados o en diferentes partes de un proyecto más grande, mantén una convención de nomenclatura consistente. | webapp_frontend y webapp_backend | webappFront y backend_for_webapp |
| Contextualizar | Si el entorno es para un cliente, un curso o un evento específico, considera incluir ese contexto en el nombre. | clientA_ml_project o springhackathon_project | ml_project o hackathon_project |

En todo caso siempre será una buena práctica nombrar al entorno virtual con el mismo nombre del proyecto.

---

### 4**. Activar y Desactivar Entornos**

Activar es el término que usa para referirse a usar un entorno virtual, entrar en el. Y deactivate para dejar de usar o salir de un entorno virtual.

Para activar un entorno:

```bash
conda activate py35
```

Para desactivar el entorno actual:

```bash
conda deactivate
```

### 5**. Ver y Gestionar Paquetes en un Entorno**

Para ver todos los paquetes en el entorno actual:

```bash
conda list
```

Para ver un paquete específico:

```bash
conda list pandas
```

Para actualizar un paquete a la versión más reciente:

```bash

conda update pandas
```

Para instalar o cambiar a una versión específica de un paquete:

```bash
conda install pandas=1.2
```

### **7. Cambiar el Nombre de un Entorno Virtual**

No hay un comando directo para renombrar un entorno en conda. Sin embargo, puedes clonar un entorno con un nuevo nombre y luego eliminar el antiguo:

```bash
conda create --name py38 --copy --clone py35
conda remove --name py35 --all
```

---

### 8. Desinstalar un paquete con Conda

Para eliminar un paquete específico de tu ambiente Conda, utiliza el siguiente comando:

```bash
conda remove [nombre_del_paquete]
```

**Ejemplo**:

Si deseas desinstalar el paquete `pandas`, ejecuta:

```bash
conda remove pandas
```

Para verificar que el paquete se ha desinstalado correctamente, puedes listar todos los paquetes y buscar el que acabas de eliminar:

```bash
conda list pandas
```

Si `pandas` se ha desinstalado correctamente, este comando no debería mostrar ningún resultado.

---

### 9. Eliminar un ambiente virtual con Conda

Antes de eliminar un ambiente, es crucial asegurarse de que no estás usando ese ambiente en ese momento. Si estás trabajando dentro de un ambiente que deseas eliminar, primero debes desactivarlo.

Para desactivar un ambiente:

```bash
conda deactivate
```

Una vez desactivado el ambiente, puedes proceder a eliminarlo con el siguiente comando:

```bash
conda env remove --name [nombre_del_ambiente]
```

**Ejemplos**:

Para eliminar un ambiente llamado `py35`, puedes usar cualquiera de las siguientes opciones:

```bash
conda env remove --name py35
```

o

```bash
conda env remove -n py35
```

Para verificar que el ambiente se ha eliminado correctamente, lista todos los ambientes disponibles:

```bash
conda env list
```

El ambiente `py35` no debería aparecer en la lista si se ha eliminado correctamente.

---

**Nota importante**: Es esencial recordar que no debes estar usando un ambiente al momento de eliminarlo. Siempre desactiva el entorno virtual antes de intentar eliminarlo para evitar errores o problemas.

---

# 5. Comandos Avanzados de Conda

> Es una buena práctica no modificar el ambiente virtual ********base********
> 

### 1. Instalación de paquetes

Para instalar un paquete específico, puedes usar el comando:

```bash
conda install [nombre_del_paquete]
```

Si el paquete no está disponible en el canal principal de Conda, puedes especificar un canal diferente, también se puede buscar el paquete en [anaconda.org](http://anaconda.org), y así saber qué canal se encuentra el paquete y posteriormente instalarlo de la siguiente manera:

```bash
conda install -c [nombre_del_canal] [nombre_del_paquete]
```

**Ejemplo**:

Para instalar el paquete `boltons` desde el canal `conda-forge`:

```bash
conda install -c conda-forge boltons
```

<aside>
📌 **Instalación de paquetes de pip en Conda**: Aunque Conda es un gestor de paquetes, también puede interactuar con pip. Si un paquete no está disponible en Conda, pero sí en pip, puedes instalarlo directamente desde Conda usando pip. Por ejemplo:

```bash
pip install pybbn
```

</aside>

---

### 2. Revisión y restauración de ambientes

Conda mantiene un registro de todas las modificaciones realizadas en tu ambiente. Puedes ver este registro con:

```bash
conda list --revision
```

Para restaurar tu ambiente a una revisión específica:

```bash
conda install --revision [número_de_revisión]
```

---

### 3. Exportación e importación de ambientes

Es posible exportar la configuración de tu ambiente para compartirlo o replicarlo en otra máquina, o para compartirlos con otras personas. Hay varias formas de hacerlo:

- El siguiente comando bash exporta una lista completa de todas las librerías e información de el ambiente virtual del ambiente virtual en el que nos encontramos

```bash
conda env export
```

- Un forma mas efectiva de hacer esto, es sólo exporta las versiones de todos los paquetes instalados, con el siguiente comando.

```bash
conda env export --no-builds
```

******************************************************************************************************************La otra forma más recomendada de hacer esto es la siguiente:******************************************************************************************************************

- Exportar solo con paquetes instalados manualmente:

```bash
conda env export --from-history
```

- El siguiente paso es exportar esta información a un archivo específico:

```bash
conda env export --from-history --file nombre_archivo.yml
```

> El nombre del archivo se puede llamar `environment` de manera general, o puede tener un nombre más específico.
> 

Y por último, si queremos volver a instalar este ambiente desde otra computadora debemos de importar el ambiente desde un archivo, de la siguiente manera:

```bash
conda env create --file nombre_archivo.yml
```

<aside>
📎 **Ambientes y .yml**: En Conda, un ambiente se refiere a un "environment". Al exportar un ambiente, se utiliza el formato .yml, que proviene de YAML ("YAML Ain't Markup Language"). Es un formato de serialización de datos legible por humanos y es ampliamente utilizado para configuraciones.

</aside>

# **6. Usando Mamba**

Mamba es una alternativa rápida y ligera a Conda, diseñada para acelerar la resolución de dependencias y la instalación de paquetes. Es especialmente útil cuando se trabaja con entornos virtuales que tienen muchas dependencias, ya que Mamba utiliza un solucionador de dependencias optimizado y escrito en C++. Aunque Mamba es una herramienta diferente, su sintaxis es idéntica a la de Conda, lo que facilita su adopción.

Para instalar Mamba, simplemente ejecuta:

```bash
conda install -c conda-forge mamba
```

Una vez instalado, puedes usar **`mamba`** en lugar de **`conda`** para la mayoría de las operaciones, como crear entornos, instalar paquetes y actualizarlos.

# **7. Buenas Prácticas con Ambientes Virtuales**

Mantener un ambiente virtual separado para cada proyecto es una excelente práctica en el desarrollo de software y ciencia de datos. Esto asegura que las dependencias de un proyecto no interfieran con las de otro, y facilita la replicabilidad y portabilidad del proyecto.

Cuando un ambiente tiene muchas dependencias, actualizar un solo paquete puede causar incompatibilidades o errores. Al dividir un proyecto en múltiples ambientes virtuales, se minimiza el riesgo de inestabilidad.

Una estructura de directorio recomendada para proyectos es:

```markdown
- data
- models
- notebooks
- **envs**
    - **external.yml**
    - **model.yml**
    - **communication.yml**
```

Dentro de la carpeta **`envs`**, puedes mantener diferentes archivos **`.yml`** que describan los ambientes para diferentes partes de tu proyecto. Por ejemplo, **`model.yml`** podría contener las dependencias necesarias para el modelado, mientras que **`communication.yml`** podría contener paquetes para la visualización o comunicación de resultados.

**Snakemake**: Una herramienta que complementa esta estructura es Snakemake, un motor de flujo de trabajo que permite definir y ejecutar tareas en un orden específico. Con Snakemake, cada paso del proyecto se puede dividir y automatizar, asegurando que todas las dependencias y tareas se manejen correctamente. Es especialmente útil para proyectos de ciencia de datos y bioinformática, donde los flujos de trabajo pueden ser complejos y constar de múltiples etapas.

[Snakemake — Snakemake 7.32.3 documentation](https://snakemake.readthedocs.io/en/stable/)